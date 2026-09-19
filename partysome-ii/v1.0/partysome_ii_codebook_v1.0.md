# PartySOME II codebook

PartySOME II is a monthly panel of political parties' issue attention (salience)
on social media, built by classifying posts from the PartySOME dataset
(Jan & Sattelmayer 2025) into Comparative Agendas Project (CAP) issue
categories. It covers 219 parties in 18 European countries on Facebook,
Twitter, and Instagram, from account creation through **2023-12**.

Classification uses PolTextLab's multilingual CAP model,
[`poltextlab/xlm-roberta-large-pooled-cap-v3`](https://huggingface.co/poltextlab/xlm-roberta-large-pooled-cap-v3)
(v3), applied off-the-shelf (not fine-tuned on this corpus — see the
paper for the model comparison and why this configuration was chosen).

Companion paper: Jan, M. & Sattelmayer, L., "PartySOME II: a dataset on
parties' issue agendas on social media" (West European Politics,
forthcoming).

## Files

- `data/partysome_ii_monthly_v1.0.csv` — party x month x issue panel,
  pooled across platforms.
- `data/partysome_ii_monthly_{facebook,twitter,instagram}_v1.0.csv` — same
  panel, broken out by platform, one file per platform.
- `data/partysome_ii_coverage_status_v1.0.csv` — one row per party, with a
  classification-coverage status per platform. See "Coverage" below.

## Variables

| Variable | Description |
|---|---|
| `party_id` | Party identifier, sourced from ParlGov.  |
| `country_name_short` | Country of the party (ISO-style 3-letter code). |
| `party_name_short` | Party abbreviation, sourced from ParlGov |
| `platform` | *(platform files only)* `facebook`, `twitter`, or `instagram`. |
| `month` | First day of the month of observation (e.g. `2015-03-01`). |
| `cap_label` | CAP issue category identifying this row (see below). |
| `n_label` | Number of posts this party published this month assigned to this `cap_label` by the CAP classifier's raw output — see "Recoding" below for how this differs from `n_label_recoded`. |
| `n_label_recoded` | Number of posts assigned to this `cap_label` under the corrected scheme (see "Recoding" below). `n_label_recoded / total_posts == cap_share_recoded` exactly, on every row. |
| `total_posts` | Total number of posts this party published this month, across all labels (same value on every row for a given party-month). |
| `cap_share` | `n_label / total_posts`. Ranges 0–1. |
| `cap_share_recoded` | `n_label_recoded / total_posts` — differs from `cap_share` see "Recoding" below. This is the paper's recommended measure. |

### CAP issue categories (22)

Agriculture, Civil Rights, Culture, Defense, Domestic Commerce, Education,
Energy, Environment, Foreign Trade, Government Operations, Health, Housing,
Immigration, International Affairs, Labor, Law and Crime, Macroeconomics,
No Policy Content, Public Lands, Social Welfare, Technology,
Transportation.

### Recoding of `cap_share_recoded`

Each post has two independent predictions: a policy/no-policy classifier
(is this substantive policy content or not?) and a separate CAP topic
classifier (which of the 21 topics does this resemble?), run regardless of
the first classifier's verdict. `cap_label` identifies the row (one of the
22 categories); `n_label` and `cap_share` are computed from the CAP
classifier's raw output, taken at face value. `cap_share_recoded` is a
*different, corrected* share for that same row: any post the
policy/no-policy classifier flagged as non-substantive is moved to
`"No Policy Content"` for this measure, regardless of whatever topic the
CAP classifier separately guessed for it; posts with no text at all are also moved to `"No Policy Content"`. This is the paper's recommended measure.

### Panel data

Each party's series spans from their own first post to their own last
post (and, in the platform files, each party-platform's own range),
not a fixed global window. Every month in that span appears with all 22
`cap_label` rows, even ones with no posts — counts and shares are
zero-filled rather than missing. There are no NaN cells anywhere in
either file.

## Coverage

| Status | Meaning |
|---|---|
| `classified` | This party-platform has classified posts in the release. |
| `not_classified` | Posts exist for this party-platform but none were run through the classifier (added to collection after the classification pipeline ran, not yet backfilled). |
| `no_account` | No posts on this platform at all. |
