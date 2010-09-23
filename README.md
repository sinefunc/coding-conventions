Sinefunc coding conventions
===========================

These are coding conventions we use internally in the joyful world of
Sinefunc, Inc.

 - [Sinefunc.com](http://sinefunc.com)
 - [github.com/sinefunc](http://github.com/sinefunc)

## HTML

 - Classes should be dasherized. (eg: `<div class='source-view'>`)

 - IDs should be underscored. (eg: `<div id='contact_label'>`)

 - On naming classes and IDs: the shorter, the better.

 - Don't repeat yourself; instead of `<a class='comment-link'>`, consider
   instead `<a class='comment'>`.

 - JS files included before `</body>`, CSS files included before `</head>`.

 - No inline CSS styles, ever.

 - Avoid classes if possible.

 - Don't use ID's (for styling purposes), unless they are layout/template
   elements (eg: `#sidebar`, `#footer`, etc).


### HTML Forms

 - Form input names should be in the form `entity[field]`,
   eg: `<input name='person[name]'>`.

 - Form input IDs (only if needed!) should be in the form `entity_field`,
   eg: `<input name='person[first_name]' id='person_first_name'>`. IDs are often
   only necessary for checkboxes.

 - Checkboxes should be done with a hidden field before it, and have
   an ID.
 
     <label for='my_id'>
       <input type='hidden' name='input_name' value='0' />
       <input type='checkbox' name='input_name' id='my_id' value='1' />
     </label>

 - Avoid stray inputs without labels.

 - IDs should never contain brackets.

 - Use `<button>` instead of `<input type='button'>`.

 - `<input>` should be inside `<label>` if possible. Same goes for `textarea`s and `select`s.

 - Use `<h3 class='legend'>` instead of `<legend>`.


## Filenames

 - Use underscores. (eg: `link_person.haml`, `comment_foo.rb`)

 - (Ruby/Python) if your file contains one class, underscorize it as the
   filename. (eg: `ContactDetail` becomes `contact_details.rb`)

 - Views for resources should be named this way:

   - `id.haml`    - For `/person/1'
   - `edit.haml`  - For `/person/1/edit`, uses the partial below
   - `form.haml`  - The form partial
   - `list.haml`  - For `/people`


## Localizations

 - Localize every string.

 - The first namespace defines the section the string is for. For instance,
   `blog_post.create: "Create"` means it's the string called `create` for
   the `blog_post` section of the application.

 - If a string you want is already defined (and is in the same namespace),
   use it instead of making a new one.
 
 - If a string you want is already defined and is in a *different* namespace,
   bring it to the global namespace first, then use it.

   For example, if you want to create `images.comments`, which happens to
   be the same as `blog_post.comments`, create a new `comments` key, and
   deprecate `blog_post.comments`.


## JavaScript

 - 2 spaces indent.

 - Always use `.live` and `.livequery`.

 - Don't use `$(function() { });` unless you really have to. Consider
   using `.live` or `.livequery`.

 - Use the jQuery include wrapper.

 - App-specific should be prefixed, eg: `lp.advanced_search.js`.


## Ruby

 - Follow [Neukichuren's guide](http://github.com/chneukirchen/styleguide/raw/master/RUBY-STYLE).
