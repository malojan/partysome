# PartySOME

PartySOME tracks how political parties communicate on social media, and
what they talk about while doing it. It combines party social media posts
with standardized policy issue classifications, enabling comparative
research on party competition and political communication across
countries, platforms, and time.

This repository holds the published, citable data releases behind the
project's two papers. A separate, actively developed website at
**[partysome.org](https://www.partysome.org/)** offers a public dashboard
for exploring what parties are talking about close to real time. That
site is in development and its underlying data is not fixed: it changes
as new data is collected, bugs are fixed, and coverage gaps are found and
addressed. It does not represent a citable release — for that, use the
frozen datasets in this repository.


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

## PartySOME II: Issue Agendas ([`partysome-ii/`](partysome-ii/), v1.0)

Monthly party-level issue salience, using the Comparative Agendas Project
(CAP) classification scheme, on Facebook, Twitter, and Instagram for 18
countries, through end of 2023.

Codebook: `partysome-ii/v1.0/partysome_ii_codebook_v1.0.md`. Companion paper: Jan,
M., & Sattelmayer, L. PartySOME II: a dataset on parties' issue agendas
on social media. *West European Politics* (forthcoming). 

```bibtex
@misc{jan_sattelmayer_2026,
  title={Issue Competition on Social Media: A new comparative dataset on Parties' issue agendas},
  url={osf.io/preprints/socarxiv/x47qr_v1},
  publisher={SocArXiv},
  author={Jan, Malo and Sattelmayer, Luis},
  year={2026},
  month={May}
}
```

## In progress

The project is actively being extended beyond these two releases via
[partysome.org](https://www.partysome.org/), currently a beta, which is
updated on an ongoing basis (as of writing, data through 2026) rather
than frozen to a single cutoff. Work in progress there includes:

- the United States added as a new country,
- collection under way for many parties on Telegram, Bluesky, and
  TikTok, in addition to the platforms in the releases above
  
None of this in-progress work is part of either release above, and its
coverage is not yet complete. It will be published as its own dataset
once stable, following the same versioning approach.

If you encounter any errors or issues, please contact malo.jan@sciencespo.fr
or open an issue on GitHub.
