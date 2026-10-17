# Openline Design and Animation Review

Openline's official review workspace for product animations, interface concepts, contextual QA, and implementation handoffs. Maintained by [Openline](https://openline.com) in [askopenline/openline-anims-review](https://github.com/askopenline/openline-anims-review).

## What this repository is

This is a review and delivery environment, not the production Openline website or mobile application. It brings alternatives, selected designs, page-context previews, acceptance criteria, and implementation notes together so design and engineering can work from the same reference.

- **Review preview:** [Animation and design review](https://openline-anims-review.vercel.app).
- **Contextual QA:** [Page-context previews](https://openline-anims-review.vercel.app/qa).
- **Delivery hub:** [Implementation handoff](https://openline-anims-review.vercel.app/delivery).
- **Company repository:** The code and documentation here are the company-maintained copy. Existing preview hosting is configured separately and is not moved by copying this repository.

## Start here

| Area | Purpose |
| --- | --- |
| [`index.html`](index.html), [`js/`](js/), [`css/`](css/) | Animation library, review controls, and shared presentation |
| [`omdm.html`](omdm.html), [`producthunt.html`](producthunt.html), [`start.html`](start.html), [`choice.html`](choice.html) | Focused product and journey concepts |
| [`qa/`](qa/) | Selected designs in page context, QA notes, and supporting assets |
| [`delivery/brief.md`](delivery/brief.md) | Web implementation brief and scope |
| [`delivery/import-guide.md`](delivery/import-guide.md) | Packaged runtime integration guidance |
| [`delivery/acceptance.md`](delivery/acceptance.md) | Acceptance and production-verification gates |
| [`delivery/checklist-guide.md`](delivery/checklist-guide.md) | Implementation checklist usage |
| [`delivery/mobile-handoff.md`](delivery/mobile-handoff.md) | Separate mobile implementation scope |
| [`delivery/followup-2026-10-09.md`](delivery/followup-2026-10-09.md) | Dated follow-up clarifications |
| [`mobile-src/`](mobile-src/), [`mobile/`](mobile/) | Mobile review source and built reference |

## Run locally

Use a current Node.js release that supports `import.meta.dirname`. The included server preserves the clean-URL behavior used by the review pages and listens only on the local loopback interface.

```sh
git clone https://github.com/askopenline/openline-anims-review.git
cd openline-anims-review
node delivery/serve.mjs
```

Open [the local delivery hub](http://localhost:8080/delivery), [the review library](http://localhost:8080), or [contextual QA](http://localhost:8080/qa). Set `PORT` if port 8080 is already in use.

For the separate mobile source:

```sh
cd mobile-src
npm ci
npm run dev
```

Run `npm run build` in that directory when preparing an updated mobile preview. Review its output before replacing committed built files.

## Review and implementation

1. Use the selected design and the relevant delivery item, not an abandoned alternative.
2. Check the animation inside its destination page for spacing, text, focus, reduced motion, and mobile behavior.
3. Keep web/shop integration and native mobile implementation as separate delivery and acceptance tracks.
4. Record implementation decisions and unresolved questions in the delivery materials.
5. Validate the integrated product, not only this reference preview. Production APIs, provisioning, payments, account state, and native behavior require their own tests.

The downloadable handoff packages are versioned snapshots. Editing source does not automatically rebuild a ZIP, update a collaborator's checkout, or deploy a production change.

## Prototype and attribution boundaries

Some flows simulate purchase-code redemption, account transitions, activation, connectivity, plan selection, or support interactions. Sample prices, network rosters, illustrative people, and successful end states are not proof of a live service, partner agreement, or production readiness.

- **Operator marks:** See the [operator asset notes](qa/assets/operators/README.md). Identification does not establish partnership or coverage.
- **AI service icons:** See the [provider attribution](qa/assets/ai/README.md). External handoffs do not imply endorsement.
- **Support portraits:** See the [illustrative portrait notes](qa/assets/support-portraits/README.md). They are not staff photographs.
- **Openline work:** Company-created designs and documentation are maintained by Openline. Third-party materials retain their own rights and notices.

For product information or company enquiries, use [Openline](https://openline.com). For repository corrections, use [this repository's issues](https://github.com/askopenline/openline-anims-review/issues).
