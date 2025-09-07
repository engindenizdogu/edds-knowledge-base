---
title: Gitbook Theme
parent: Jekyll
---

##### Creating a section
1. **Add collection definition to `_config.yml`:**

```
collections:
  pages:
    output: true
    permalink: /:collection/:path/
  new_section: # ADD THIS
    output: true
    permalink: /:collection/:path/
```

2. **Create folder:** `_new_section`. It should start with an underscore. The name of the folder and the name of the section should match
3. **Add content:** Put .md files in _test/
4. **Order control:** Update the `ordered_collections` configuration

```
ordered_collections:
  - posts
  - pages
  - others
  - new_section
```

##### Removing a section
1. Remove from`_config.yml` (both from *collections* and *ordered_collections*)    
2. Remove `_new_section` folder entirely
3. Run `bundle exec jekyll clean` or delete `_site` folder entirely

```
bundle exec jekyll clean
```

- If you're using GitHub Pages or similar, you may need to trigger a rebuild.
- Search your codebase for any hardcoded references to the collection name
- Check if any other files link to pages in that collection