# azure-api-management-docs-as-flashcards

Instructions to download [the Anki flashcard deck can be found by clicking here](https://github.com/asa55/azure-api-management-docs-as-flashcards/releases/), or by navigating to the Releases area of this project. To see what content will be added in the future, [check out this project's Roadmap by clicking here](https://github.com/users/asa55/projects/14). 

## What this repository does

This repository contains (1) Markdown files and (2) a GitHub Actions workflow definition that converts Markdown into an Anki-compatible flashcard deck. The build process can be triggered manually under the Actions tab, and generates a single build artifact, a `.apkg` file that you can import directly into Anki.

## What this repository is

The content of the flashcards defined within the Markdown files in this repository reflects the content of the official Microsoft documentation for Azure API Management, which can be found here: [`https://learn.microsoft.com/azure/api-management/`](https://learn.microsoft.com/azure/api-management/).

For those familiar with Anki flashcards, and specifically the concept of tags, the way this flashcard deck is organized will be of interest to you. If you follow the above link to the Azure docs (on the desktop version of the website) you'll notice that the docs are organized hierarchically. For example, there is a section called `Overview` with a subsection named `About API Management`. In keeping with this convention, each flashcard derived from this subsection is tagged with both `Overview` and `Overview::About-Azure-API Management`. All flashcards are tagged according to this convention. So if you want to limit your study session to a particular area of the official Microsoft documentation, you may easily do so by selecting the tag corresponding to the section or subsection that interests you.

## Why this repository exists

Docs are boring, but very important. If you want to learn anything fast, or deeply, rote memorization is an important step in the process.

Flashcards are one great way to pound basic bits of information into your brain, and retain massive volumes of information. Anki by far the most popular free and open-source flashcard app around, available for both desktop and mobile.

This is exactly where `*-docs-as-flashcards` comes in. I've taken the documentation and converted the critical information into a flashcard format, so that you and/or your team can study-up as quickly and efficiently as possible, then go off and confidently use these technologies to achieve what you've set out to achieve.

## Notes

- I maintain these flashcards manually
  - As such, the scope of what the flashcards cover are currently prioritized according to what I need personally
  - Manual updates can become dated quickly, as Azure docs are continuously updated
    - If you notice any inconsistencies with the docs over time, please feel free to file an issue and I'll look into making updates
    - Also, on the topic of issues, you'll quickly see how I'm prioritizing what docs get transcribed into flashcards using a convention that aligns directly with the tagging convention
      - By navigating the issues, you'll be able to see if the documentation page you're interested in has been transcribed into flashcards or not
      - If there's something you want to see that's not available yet, go to the appropriate issue for the docs you're looking for and let me know it interests you by leaving a comment or a :+1:.
- This project leverages v2.0.0 of [`md2apkg-run`](https://github.com/asa55/md2apkg-run) to build Anki-compatible flashcard deck out of the `.md` flashcard definition files underneath the `Deck/` folder.
- If you find these flashcards helpful and want to see more, faster, let me know
  - Once these flashcards reach a minimum level of maturity, I'll set up a donation button / Patreon page that you can use to help guide my priorities and help me keep this content aligned with the latest changes to the Microsoft docs
