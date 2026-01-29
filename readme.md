# QA Case Study

This repo shows how I approach testing - from analyzing what needs testing to designing test cases and figuring out what should be automated. The goal here isn't to write every possible test, but to show how I think about QA, spot risks, and communicate clearly.

## What's Inside
- `case.md` – testing approach, what I'm covering (and what I'm not), assumptions I made, and how I read the results
- `manual/` – The actual test cases I'd run by hand, including edge cases and functional scenarios
- `automation/` – Which tests I think should be automated and why

## How I Work
- I write manual tests in Markdown because it's simple and easy to track
- For automation, I pick the tests that catch regressions and matter most - wrote these with Playwright in mind