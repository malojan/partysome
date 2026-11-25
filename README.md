# PartySOME

PartySOME tracks how political parties communicate on social media, and
what they talk about while doing it. It combines party social media posts
with standardized policy issue classifications, enabling comparative
research on party competition and political communication across
countries, platforms, and time.

This repository holds the published, citable data releases behind the
project's two papers.

## partysome.org

**[partysome.org](https://www.partysome.org/)** is the project's public
website, updated every day. It covers parties in 38 countries on
Facebook, X/Twitter, Instagram, YouTube, TikTok, Telegram and Bluesky:
how much they post, what they talk about (the policy issues each party
emphasises, for 22 countries), and their audience (followers and
engagement with their posts). It is available in English, French and
German.

The website's data changes as new posts are collected and as errors are
found and corrected, so it is not a citable release. For research, use
the frozen datasets in this repository.


## PartySOME: Social Media Activity ([`partysome/`](partysome/), v1.0)

Posting volume and timing on Facebook, Instagram, Twitter, and YouTube
for 37 countries, account creation through end of 2023.

Codebook: `partysome/v1.0/partysome_codebook_v1.0.pdf`. Companion paper: Jan, M., &
Sattelmayer, L. (2025). PartySOME: A comprehensive dataset on political
parties' SOcial MEdia activity. *Party Politics*.
https://doi.org/10.1177/13540688251388763

```bibtex
@article{Jan_2025,
  title={PartySOME: A comprehensive dataset on political parties’ SOcial MEdia activity},
  ISSN={1460-3683},
  url={http://dx.doi.org/10.1177/13540688251388763},
  DOI={10.1177/13540688251388763},
  journal={Party Politics},
  publisher={SAGE Publications},
  author={Jan, Malo and Sattelmayer, Luis},
  year={2025},
  month=oct
}
```

## PartySOME II: Issue Agendas ([`partysome-ii/`](partysome-ii/), v2.0 and v1.0)

Monthly party-level issue salience, using the Comparative Agendas Project
(CAP) classification scheme.

- **v2.0** (current): 268 parties in 22 countries (the 18 of v1.0 plus
  Australia, Canada, New Zealand and the United States), on Facebook,
  Twitter, Instagram, TikTok, Telegram and Bluesky, through October 2026.
  Codebook: `partysome-ii/v2.0/partysome_ii_codebook_v2.0.pdf` (also as
  `.html`), which also describes the differences from v1.0. The release
  includes the hand-coded validation sample (post ids and labels). The
  hand-coded posts used to train the policy classifier and to validate
  both classifiers, with their texts, are available on request.
- **v1.0**: 219 parties in 18 countries, on Facebook, Twitter and
  Instagram, through end of 2023. This is the version used in the
  companion paper. Codebook:
  `partysome-ii/v1.0/partysome_ii_codebook_v1.0.md`.

Companion paper: Jan, M., & Sattelmayer, L. (2026). PartySOME II: a
dataset on parties' issue agendas on social media. *West European
Politics*, 1–20. https://doi.org/10.1080/01402382.2026.2734520

```bibtex
@article{jan_sattelmayer_2026,
  title={PartySOME II: a dataset on parties' issue agendas on social media},
  author={Jan, Malo and Sattelmayer, Luis},
  journal={West European Politics},
  pages={1--20},
  year={2026},
  publisher={Taylor \& Francis},
  doi={10.1080/01402382.2026.2734520},
  url={https://doi.org/10.1080/01402382.2026.2734520}
}
```

If you encounter any errors or issues, please contact malo.jan@sciencespo.fr
or open an issue on GitHub.
