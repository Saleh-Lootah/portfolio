---
title: Rethinking the color taxonomy of this website
date: 2024-04-08
description: "New color taxonomy for salehlootah.com explained"
url: /colors
---
### What did I do?

I just spent a significant amount of time re-thinking the taxonomy of the color system of this website. In the grand scheme of things this realistically is pointless because no one is going to know, nor is anyone else going to be working on my website, so clearer naming and more intuitive color classification is not really that important, but who gonna stop me?

### Okay, why though?

If you take a look at the the main style sheet before commit [4a514b8](https://github.com/saleh-lootah/portfolio/commit/4a514b8bb018c0497976f6b1b2a483aafea46647) you'll find that the colors were divided into 3 main categories: base, primary and on-primary

```
--base-1: var(--cream-50);
--base-2: var(--cream-100);
--base-3: var(--cream-200);
--base-frosted-glass: rgba(255 255 255 / 50%);

--primary: var(--cream-950);
--on-primary: var(--cream-200);

--primary-hover: var(--cream-200);
--primary-active: var(--cream-700);

--on-primary-hover: var(--cream-950);
--on-primary-active: var(--cream-200);
```

This is very loosely based on google's material design color taxonomy, where base is synonomous with surface in the afforementioned color system.

Given that one of my goals is to keep the website minimal as possible I cherry picked the colors I actually needed to comfortably implement a dark mode as well as have room to integrate themes into the webiste in the future. All this is nice, but why did I take the time to update the variables? The honest answer is that I felt that I could do better and figured why not. So this is what I came up with:

```
--base: var(--cream-50);
--base-hover: var(--cream-200);
--base-active: var(--cream-300);
--base-focused: var(--yellow);
--base-disabled: var(--cream-100);
--base-inverse: var(--cream-950);
  
--content: var(--cream-950);
--content-hover: var(--cream-950);
--content-active: var(--cream-950);
--content-focused: var(--gray-950);
--content-disabled: var(--cream-400);
--content-inverse: var(--cream-200);
```

The updated color taxonomy reduces the categories to 2: base and content. I removed the frosted glass variable and added variables for the focused state and for inversing base and content. While the variable count has increased due to the newly introduced states, the categorization has been simplified. Everything that's a background is base, everything that goes on top of a background is content, pretty simple.

### Ok, Cool

So yeah, a miniscule change that no one can really see nor which has a real impact on anything really, but I can sleep better now that I have cleaned it up and simplified it. Now I am probably going to face an issue with code block styling.
