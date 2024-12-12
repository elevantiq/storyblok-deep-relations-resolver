<p align="center">
  <a href="https://www.elevantiq.com">
  <picture >
    <source media="(prefers-color-scheme: dark)" srcset="https://github.com/elevantiq/.github/raw/main/brand/logo-light.png">
    <source  media="(prefers-color-scheme: light)" srcset="https://github.com/elevantiq/.github/raw/main/brand/logo-dark.png">
    <img height="40" width="auto" alt="Elevantiq Logo" src="https://github.com/elevantiq/.github/raw/main/brand/logo-dark.png">
    </picture>
  </a>
</p>

<h1 align="center">
  Storyblok Deep Relations Resolver
</h1>

<p align="center">
The Storyblok Deep Relations Resolver is a TypeScript library that resolves relations on <i>more than 2 levels</i> in Storyblok's API responses. It enables developers to 
easily access nested data from the API responses, making it easier to
work with complex data structures.
</p>
<p align="center">
    <img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat" alt="PRs welcome!" />
  <a href="https://x.com/intent/follow?screen_name=elevantiq">
    <img src="https://img.shields.io/twitter/follow/elevantiq.svg?label=Follow%20@elevantiq" alt="Follow @elevantiq" />
  </a>
</p> 

## Installation

To install the package, run the following command:

```bash
npm install @elevantiq/storyblok-deep-relations-resolver

# or with yarn

yarn add @elevantiq/storyblok-deep-relations-resolver
```

## Usage

To use the package, simply import it into your project and use the resolve function to resolve the deep relations in
your Storyblok API responses.

```typescript
import {resolveRelationsDeep} from '@elevantiq/storyblok-deep-relations-resolver'

const storyblokApi = getStoryblokApi()

// format: <component>.<field>
export const deepRelations = [
    'articlesTeaser.articles',
    'article.author',
    'article.category',
    'primaryContactTeaser.contactPerson',
]

const {data: preResolveData} = await storyblokApi.get(`cdn/stories/${slug}`, sbParams)

const deepResolvedData = await resolveRelationsDeep(storyblokApi, preResolveData, deepRelations)
```

For more information on how to use the package, see the documentation.

## Contributing

If you would like to contribute to the project, please follow these steps:

- Fork the repository
- Create a new branch for your changes
- Make your changes and commit them with clear commit messages
- Push your changes to your forked repository
- Submit a pull request

## License

This project is licensed under the [MIT License](./LICENSE.md).

## Reporting Bugs

If you find any bugs or issues with the package, please report them by creating a new issue on the GitHub issue tracker.

## Contact

If you have any questions or feedback, feel free to contact us at our GitHub profile.
