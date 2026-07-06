# Contributing to Weaving Type

Thanks for wanting to improve Weaving Type. Issues and pull requests are both welcome.

## Reporting issues

Open an issue with:
- What you expected vs. what happened.
- Your **TouchDesigner build** (e.g. 2023.30060) and OS.
- The **Source** type and any relevant parameter settings.
- A screenshot or short screen recording if it's visual.

Feature ideas and questions are fine as issues too.

## Submitting changes (pull requests)

Weaving Type ships as a single **binary component** (`weaving_type.tox`), so PRs work a little differently from a text codebase:

1. **Fork** this repository and clone your fork.
2. Open `weaving_type.tox` in TouchDesigner, make your change, and **re-save the component** over the same file (right-click the component → *Save Component .tox*).
3. Commit the updated `weaving_type.tox`.
4. Open a pull request and **describe the change in detail** — because the `.tox` is binary, the diff won't be readable, so the description does the work:
   - What you changed and why.
   - Which operators / parameters / scripts you touched (paths inside the component).
   - **Before / after** screenshots or a short clip.
   - Anything that affects performance or existing behaviour.

Keep pull requests focused on one change where you can — it makes review much easier.

## Review

The maintainer reviews each PR against the working component before merging. Because the file is binary, expect changes to be re-created or verified inside TouchDesigner rather than merged blindly.

## Licensing of contributions

By submitting a pull request you agree that your contribution is provided under the project [`LICENSE`](LICENSE), and that ownership of the merged work remains with Nicholas Marriott (nicholaspjm).
