# Rosie - Customizable AIML Chatbot Base

Rosie is a comprehensive collection of AIML and AIML 2.0 files designed to serve as a robust foundation for any chatbot project. It is a specialized fork of the renowned ALICE 2.0 project, meticulously optimized for seamless deployment and operation on the Pandorabots platform. Rosie provides a ready-to-use conversational core, enabling developers to quickly launch and customize intelligent chatbots.

## Features

*   **Extensive AIML Knowledge Base:** Comes pre-loaded with a broad range of conversational categories covering general knowledge, personality, basic inquiries, date/time, and more.
*   **Modular Design:** The knowledge base is structured into numerous AIML files, each focusing on specific domains (e.g., `animal.aiml`, `date.aiml`, `personality.aiml`), facilitating easy customization and extension.
*   **Bot Profile Management:** Includes sophisticated categories for defining and retrieving bot-specific attributes like name, age, gender, location, hobbies, and more, enabling a personalized bot persona.
*   **User Profile Interaction:** Categories for client profile allow for more personalized interactions based on user input.
*   **Linguistic Processing:** Utilizes AIML `maps`, `sets`, and `substitutions` to handle diverse linguistic patterns, pluralizations, conjugations, and contextual understanding, enhancing conversational flow and accuracy.
*   **Pandorabots Optimization:** Specifically tailored for the Pandorabots platform, ensuring compatibility and leveraging its features.
*   **Dynamic Updates:** Designed for straightforward updates, with new content frequently introduced in `z_update.aiml` to allow existing users to integrate improvements without overwriting custom work.
*   **GNU GPLv3 Licensed:** Freely available for use, modification, and distribution under the terms of the GNU General Public License Version 3.

## Tech Stack

*   **AIML (Artificial Intelligence Markup Language):** The core technology for defining the chatbot's conversational patterns and responses. Rosie utilizes both AIML and AIML 2.0 features for advanced capabilities.
*   **Pandorabots Platform:** The cloud-based platform for hosting, deploying, and managing AIML-based chatbots, for which Rosie's content is optimized.

## Installation Instructions

To get Rosie up and running, follow these steps:

1.  **Create a Pandorabots Account:** If you don't already have one, create an account on [Pandorabots](https://www.pandorabots.com).
2.  **Create a New Bot:** Once logged in, create a new bot on the Pandorabots platform.
3.  **Upload Files:**
    *   Navigate to the `lib` directory within this project.
    *   Upload all the files found under the `lib/aiml`, `lib/maps`, `lib/sets`, `lib/substitutions`, and `lib/system` directories to your newly created bot on Pandorabots.
    *   Alternatively, you can select the "Small Talk" content option within the Pandorabots interface, which often includes a version of Rosie's base content.

## Usage Instructions

Once installed, your bot will be ready for interaction on the Pandorabots platform.

*   **Interacting with Rosie:** You can test your bot through the Pandorabots UI or integrate it into various channels (web, mobile, messaging apps) using the Pandorabots API.
*   **Customizing Rosie:**
    *   To personalize Rosie, start by modifying values in `rosie.properties` (located in `lib/system/`). This file often contains key bot attributes.
    *   You can edit existing `.aiml` files in the `lib/aiml` directory to change or expand conversational responses.
    *   Add new `.aiml` files to introduce entirely new topics or functionalities.
    *   Modify `maps`, `sets`, and `substitutions` to fine-tune linguistic processing.
*   **Updating Rosie:** We periodically push improvements and new content. Unless otherwise noted, future updates will primarily be placed in `lib/aiml/z_update.aiml`. To integrate these updates without affecting your custom modifications, simply upload *only* the `z_update.aiml` file to your bot on Pandorabots.

For a more detailed description of Rosie's contents and customization tips, please refer to the [introductory blog post](http://blog.pandorabots.com/rosie-customizable-base-content/) on the topic.

## Project Structure

The project is organized into several directories, primarily under `lib/`, each serving a specific function in building the chatbot's intelligence:

```
.
├── .gitignore          # Specifies intentionally untracked files to ignore.
├── LICENSE             # GNU General Public License Version 3.0.
├── README.md           # This README file.
└── lib/                # Contains all the core AIML and configuration files.
    ├── aiml/           # Core AIML files defining conversational categories.
    │   ├── animal.aiml
    │   ├── bot_profile.aiml
    │   ├── client_profile.aiml
    │   ├── config.aiml
    │   ├── date.aiml
    │   ├── default.aiml
    │   ├── dialog.aiml
    │   ├── inappropriate.aiml
    │   ├── inquiry.aiml
    │   ├── insults.aiml
    │   ├── knowledge.aiml
    │   ├── personality.aiml
    │   ├── profanity.aiml
    │   ├── reductions1.aiml
    │   ├── reductions2.aiml
    │   ├── reductions_update.aiml
    │   ├── roman.aiml
    │   ├── that.aiml
    │   ├── train.aiml
    │   ├── udc.aiml
    │   ├── utilities.aiml
    │   └── z_update.aiml      # File designated for future updates.
    ├── maps/           # Files containing key-value mappings for linguistic transformations.
    │   ├── be2been.map
    │   ├── be2being.map
    │   ├── be2is.map
    │   ├── be2was.map
    │   ├── been2be.map
    │   ├── being2be.map
    │   ├── capital2nation.map
    │   ├── capital2state.map
    │   ├── colormap.map
    │   ├── er2est.map
    │   ├── est2er.map
    │   ├── familiargender.map
    │   ├── familiarpredicate.map
    │   ├── familiarpronoun.map
    │   ├── gendermap.map
    │   ├── gendername.map
    │   ├── is2be.map
    │   ├── name2number.map
    │   ├── nation2capital.map
    │   ├── next.map
    │   ├── number2name.map
    │   ├── number2ordinal.map
    │   ├── opposite.map
    │   ├── ordinal2number.map
    │   ├── phonetic.map
    │   ├── profile2predicate.map
    │   ├── rhyme.map
    │   ├── sign2date.map
    │   ├── state2capital.map
    │   ├── state2largestcity.map
    │   ├── tomorrow.map
    │   └── was2be.map
    ├── sets/           # Files defining sets of words or phrases for pattern matching.
    │   ├── animal.set
    │   ├── animals.set
    │   ├── article.set
    │   ├── be.set
    │   ├── been.set
    │   ├── being.set
    │   ├── bird.set
    │   ├── color.set
    │   ├── digit.set
    │   ├── entity.set
    │   ├── erdown.set
    │   ├── erup.set
    │   ├── estdown.set
    │   ├── estup.set
    │   ├── evildoers.set
    │   ├── familiarname.set
    │   ├── fastfood.set
    │   ├── food.set
    │   ├── gender.set
    │   ├── interest.set
    │   ├── is.set
    │   ├── language.set
    │   ├── letter.set
    │   ├── modal.set
    │   ├── month.set
    │   ├── name.set
    │   ├── nation.set
    │   ├── numbername.set
    │   ├── ordinal.set
    │   ├── place.set
    │   ├── preposition.set
    │   ├── profile.set
    │   ├── pronoun.set
    │   ├── quantifier.set
    │   ├── spatialprep.set
    │   ├── sphere.set
    │   ├── starsign.set
    │   ├── state.set
    │   ├── was.set
    │   ├── weekday.set
    │   ├── wet.set
    │   └── wh.set
    ├── substitutions/  # Files containing substitution rules for pre-processing input or post-processing output.
    │   ├── denormal.substitution
    │   ├── gender.substitution
    │   ├── normal.substitution
    │   ├── person.substitution
    │   └── person2.substitution
    └── system/         # System-level configuration files for the bot.
        ├── rosie.pdefaults
        └── rosie.properties
```

## Architecture

Rosie's architecture is built around the core principles of AIML, facilitating a highly structured and modular approach to chatbot development:

*   **Declarative Knowledge Representation:** The primary intelligence of the bot is defined through AIML categories, where `pattern` tags match user input and `template` tags provide the corresponding responses.
*   **Pattern Matching Engine:** An underlying AIML interpreter (provided by Pandorabots) processes user input by matching it against the vast network of categories to find the most appropriate response.
*   **Linguistic Processing Pipeline:**
    *   **Substitutions:** Input undergoes normalization (e.g., `normal.substitution`) to standardize phrasing and gender transformations (`gender.substitution`), ensuring consistent pattern matching.
    *   **Sets:** Categorized lists of words (`animal.set`, `color.set`, `name.set`) are used within AIML patterns to match a variety of user inputs efficiently without explicitly listing every possible word.
    *   **Maps:** Key-value pairs (`be2been.map`, `capital2nation.map`) are utilized for complex linguistic transformations, such as verb conjugations, geographical lookups, or other data relationships.
*   **Contextual Memory (`that`):** The `that.aiml` file and inherent AIML features allow the bot to remember the previous turn's output, enabling more coherent multi-turn conversations.
*   **Bot and Client Profiles:** `bot_profile.aiml` and `client_profile.aiml` manage dynamic variables that store information about the bot and the current user, allowing for personalized interactions and persistent memory across conversations.
*   **Modular Content Domains:** The `aiml/` directory is logically segmented (e.g., `animal.aiml`, `date.aiml`, `personality.aiml`), allowing for easier maintenance, expansion, and isolation of conversational topics.
*   **System Configuration:** `rosie.properties` and `rosie.pdefaults` provide crucial configuration parameters and default values for the bot's operation and behavior.