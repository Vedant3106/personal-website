# Project Structure

A map of this project's folders. Folders marked *(empty)* only hold a `.gitkeep` file so Git keeps them; they get filled in as the site is built.

```
./
├── public/                  Files served as-is
│   ├── fonts/               (empty)
│   ├── images/
│   │   ├── porter/          (empty)
│   │   ├── bandage/         (empty)
│   │   ├── 2070s/           (empty)
│   │   └── craft/           (empty)
│   └── videos/
│       ├── porter/          (empty)
│       ├── bandage/         (empty)
│       ├── 2070s/           (empty)
│       └── craft/           (empty)
├── src/                     All the code you write
│   ├── app/                 Pages and routes (the App Router)
│   │   ├── about/           (empty)
│   │   └── work/
│   │       ├── porter/      (empty)
│   │       ├── bandage/     (empty)
│   │       ├── 2070s/       (empty)
│   │       └── craft/       (empty)
│   ├── components/          Reusable building blocks
│   │   ├── ui/              (empty)
│   │   ├── case-study/      (empty)
│   │   └── interactive/     (empty)
│   ├── content/             (empty)
│   ├── styles/              (empty)
│   └── lib/                 (empty)
├── CLAUDE.md                Instructions for Claude (written by you)
├── STRUCTURE.md             This file
├── package.json             Project name, scripts, and dependencies
└── next.config.mjs          Next.js settings
```

## What each folder is for

**public/** holds files that are sent to the browser exactly as they are, so `public/images/a.png` is available at `/images/a.png`.
**public/fonts/** holds font files you host yourself.
**public/images/** holds pictures, with one subfolder per case study so each project's images stay together.
**public/videos/** holds video files, again with one subfolder per case study.

**src/** is the home for all the code you write, kept apart from config files at the project root.
**src/app/** is where pages live, and each folder inside it becomes a URL on your site.
**src/app/about/** will become the `/about` page.
**src/app/work/** groups your case studies under `/work/...`, with one folder per project.
**src/components/** holds reusable pieces of the interface, like a button or a gallery, that pages can share.
**src/components/ui/** is for small, general pieces such as buttons, links, and tags.
**src/components/case-study/** is for pieces used only to lay out case-study pages.
**src/components/interactive/** is for pieces that react to the visitor, such as sliders, video players, and animations.
**src/content/** is where the written case-study content (later, MDX files) will be kept, separate from the code.
**src/styles/** is where shared CSS files will go.
**src/lib/** is for small helper functions that aren't visual, such as one that loads and sorts your case studies.

## Files the starter created (not listed above)

- `src/app/layout.js`, `page.js`, `globals.css`, `page.module.css`, `favicon.ico`: the default starter page. These will be replaced as you build.
- `jsconfig.json`: lets you import with `@/` as a shortcut for `src/`.
- `eslint.config.mjs`: rules for the code checker (`npm run lint`).
- `.gitignore`: tells Git which files to skip, such as `node_modules` and `.next`.
- `node_modules/` and `.next/`: installed packages and build output. Generated automatically, never edited by hand.
