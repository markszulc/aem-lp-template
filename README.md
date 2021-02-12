# AEM Landing Page Template

This is the basic landing page template for Adobe Experience Manager as a Cloud Service (AEMaaCS).

<img src="previews/site.png?raw=true" alt="Basic site preview" width="50%">

It's (heavily) inspired by the Namari Landing Page template on https://shapingrain.com/free-landing-page-template/ but based on AEM Core Components and no custom coding. At this stage its still lacking the fancy animations & parallex scrolling.. 

## Structure

* `previews`: Folder with screenshots of the site template.
* `site`: Content package of the content that will be copied for each site created from this template (templates, pages, etc.).
* `theme`: Sources of the template theme to modify how the site looks (CSS, JS, etc.).

## Install on AEMaaCS

* Go to <https://github.com/adobe/aem-site-template-basic/releases/latest> and download `aem-site-template-basic-{version}.zip`
* Upload `aem-lp-template-{version}.zip` in AEMaaCS's site creation wizard to create a new site from that template.

## Build locally

Alternatively you can build `aem-lp-template-{version}.zip` locally.

1. Install Maven (to be able to use the packaging script).
1. Initialize the project with following command executed at the template root:

   ```bash
   npm install
   ```

1. To build the site template, run following command executed at the template root:

   ```bash
   npm run build
   ```

1. The site template ZIP file is now located below the template root: `aem-lp-template-{version}.zip`.
1. Upload to an AEMaaCS site creation wizard. For installing on a local cloudready development instance use `npm run deploy`.

## Develop Site Template

See: <https://github.com/adobe/aem-site-template-builder>

## Release

Run `Build and release` GitHub workflow and provide the semantic version you're about to release. The workflow executes the following steps:

* Build Site Template
* Release latest version on github
* Commit, build and release latest Site Theme related changes in [Site Theme E2E Repo](https://github.com/adobe/aem-site-template-basic-theme-e2e).
