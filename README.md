# Boxy (ex-Storelift)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Boxy, operated by the French company SAS Storelift (founded 2018 in Ivry-sur-Seine by David Gabai and Tom Hayat), built unstaffed 24/7 convenience stores inside 15–20 m² shipping containers. Computer vision, weight-sensing shelves and an on-site compute node let a shopper unlock the door with a QR code from the Boxy app, take products off the shelf and walk out to be invoiced automatically. The company raised ~€5M in 2020 and a €25M Series A in February 2022 led by Serena, with CapHorn and LocalGlobe, targeting 1,000 stores.

## Status: defunct — no API surface

Boxy closed its entire store estate by the end of April 2024. SAS Storelift (SIREN 838729192) entered **liquidation judiciaire on 6 November 2024**, after *sauvegarde* (June 2024) and *redressement* (September 2024) procedures; the store containers were auctioned in early 2025.

The company never published a developer program, API documentation, or a machine-readable contract, and there is nothing left to probe:

| Probe | Result |
|---|---|
| `getboxy.co` nameservers | `ns1/ns2.parkingcrew.net` — parked |
| `https://www.getboxy.co/` | TLS handshake failure |
| `http://www.getboxy.co/` (and every path probed) | `410 Gone` (ParkingCrew error page `PC410NAML1`) |
| `storelift.com` (predecessor brand) | domain-for-sale lander; soft-200 catch-all on every path |
| First-party GitHub org / npm / PyPI packages | none found |

Recorded absences live in [`well-known/getboxy-well-known.yml`](well-known/getboxy-well-known.yml) (15 paths across 3 hosts, zero real documents) and [`security/getboxy-domain-security.yml`](security/getboxy-domain-security.yml). No `WellKnown`, `AgentCard`, `OpenAPI`, or other presence pointer is wired into `apis.yml`, because none of those surfaces exist.

Source: portfolio company of [serena](https://github.com/api-evangelist/serena) — https://www.getboxy.co/ (now parked)
