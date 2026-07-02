# Palcera Base

The **site recipe** behind [Palcera CMS](https://github.com/palcera/palcera_cms): a
`type: Site` Drupal recipe providing the Schema.org content model (Person, Article,
Service, General Page), Canvas page regions/templates/pages, views, SEO configuration,
search, and demo content for a professional-services brochure site.

## Usage

Normally installed via the Palcera CMS project template (see that README). Standalone,
on any Drupal CMS 2.1+ codebase:

```bash
composer config minimum-stability dev && composer config prefer-stable true
composer require palcera/palcera_base
drush site:install --yes --site-name="My Site" <path-to>/recipes/palcera_base
```

Requires Drupal core ^11.4 (fresh-install fixes for core 11.4 landed in 1.0.0-beta4).

## Structure

- `recipe.yml` — `type: Site`; composes the Drupal CMS foundation recipes, installs the
  Schema.org stack + Palcera theme, applies config actions (front page, theme, search)
- `config/` — content types, fields, Schema.org mappings, Canvas components/regions/
  templates, views, metatags
- `content/` — demo content (nodes, media + images, taxonomy, menu links, Canvas pages)

## License

GPL-2.0-or-later.
