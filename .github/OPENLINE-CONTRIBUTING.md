# Contributing to Openline Design Review

This guide covers Openline-maintained changes in the official company repository. It supplements rather than replaces any preserved upstream contribution policy.

## Start with the project

Read the [project README](../README.md) and the guide for the area you intend to change. Keep a contribution focused on one reviewable outcome and explain its intended effect.

## Local workflow

1. Create a branch from the current `master` company branch.
2. Make the smallest complete change that addresses the issue.
3. Run the relevant checks and inspect the actual output.
4. Update affected documentation, previews, and prepared resources together.
5. Open a pull request with the change, evidence, limitations, and rollback considerations.

## Project checks

- Run the local delivery server and inspect the changed review surface.
- Test desktop/mobile layout, keyboard focus, and reduced-motion behavior.
- Update matching handoff notes and prepared downloads when their inputs change.
- Keep web and mobile acceptance tracks distinct.

## A useful pull request

Include the purpose, affected surfaces, validation performed, and any remaining acceptance gate. Screenshots or captures should show the actual changed interface and clearly identify sample data or prototype behavior.

Do not claim a build, native-device test, production check, or external-service verification that was not performed. A visual reference and an integrated working feature are different deliverables.

## Company and upstream boundaries

Preserve licenses, copyright notices, source citations, and legitimate contributor attribution. Openline-specific branding does not reassign ownership of an upstream dependency.

Keep secrets, customer information, private access codes, and production data out of commits and public discussions. Use the [company security guide](OPENLINE-SECURITY.md) for sensitive matters.

## Publication

A source change does not automatically authorize a production deployment, new external permission, or confidential-content publication. Follow the project's approved release process and record the result in the [company changelog](../OPENLINE-CHANGELOG.md).
