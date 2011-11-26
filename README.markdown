This is the inaugural [Gitstuff](http://gitstuff.com) site. You can see it at [http://gitstuff.com/jkriss/drinks](http://gitstuff.com/jkriss/drinks).

Gitstuff is kind of like Tumblr, but with everything stored in Github, and you can have whatever metadata you want. And it's searchable, including the metadata.

### File structure

These things follow a very simple structure:

- Posts go in /posts
- Layouts go in /layouts
- Assets go in /assets

Individual posts have metadata up top, and content on the bottom, much like [Jekyll](https://github.com/mojombo/jekyll).

Gitstuff expects two layout files, `page.html.liquid` and `post.html.liquid`. They use (you guessed it), [Liquid markup](http://liquidmarkup.org/).

### Variables

The post template is passed all of the metadata for your post, plus the content after the metadata (as the `content` variable). In addition, there are some extra bits.

#### Git-derived
- author.name, author.email, and author.gravatar
- created_at
- modified_at

#### Context information
- single_post (true or false)
- search_form (an html snippet for the search form)
- query (the current search query, if present)
- root_path (the url for the home page)
- asset_path (the base path for assets)
- previous_page (the link to the previous page of results, if applicable)
- next_page (the link to the next page of results, if applicable)