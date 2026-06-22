# Models

This is part ot the larger project Civ VII + AI (Kevin – ChatGPT) that is an experiment setup to explore exotic Civ VII strategies. See [README.md](./README.md) and [COLLABORATE.md](COLLABORATE.md) for further details on the overall project.

This document consists of 3 sections that form prerequisite steps that must be done before a new model can be created. The purpose is to use this to improve model clarity by defining high level requirements & for validating model use cases to ensure that they represent real game-world utility, and defining a flow for model creation from cradle to grave.

When prerequisite steps have been approved, we define new taxonomy types if needed in [models_taxonomy.json](models_taxonomy.json) and finally implement the model in [models.md](models.md) and validate the model according to validation rules stated in the model definition, see example below or in models.md. There is currently no model schema in place and no immediate plans to implement one, its purpously loosely structured to allow for quick iterations.

Deployment is literally knocking on the door to your friendly AI bot to tell them that there is a new model or a model update. The bot should know where to find this documentation and other files as need to consume the model and start producing results for regular usage and validation with user input from game if needed.

Example:

1: `models.md`

```md

```

2: `models_taxonomy.json`

```json
{}
```

```json
{}
```

## Flow

The purpose of this document is to present some general rules for model creation and maintains that will ensure that we are only creating model definitions if there are real game-world use cases that could be helped common use cases that presents specific choices that can be hard to quantify. Usually I will pick either the one that "looks good" or the one that I read about on Reddit being the best. The scientific rigor is strong in other words.

## Acceptance Criteria

A new model SHALL meet one OR two of the following high level criteria in order to pass and approved for implementation.

## Rules

These rules must be followed when creating a new model, or when updates are made to an existing mode.

- A use casse MUST be defined beforex

## Use Cases
