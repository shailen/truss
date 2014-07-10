# Truss: a framework for scaffolding Polymer apps

`Truss` is a Polymer app that generates other Polymer apps.

Consider a 'Blog' app with the following data models:

[{Post: {
    fields: [
      {name: "title", type: "String", max_length: 30, required: true},
      {name: "body", type: "String", max_length: 300, required: true},
      {published: "DateTime"},
      {comments: "OneToManyField(Comment)"},
      {tags: "ManyToManyField(Tag)"}]
    }
  },

  {Comment: {
    fields: [
      {body: "String", max_length: 300, required: true},
      {published: "DateTime"}]
    }
  },

  {Tag: {
    fields: [
      {name: "String", max_length: 20, required: true, unique: true}]
    }
  }
]

`Truss` scaffolds a Polymer app that performs CRUD operations on Post, Comment,
and Tag.

## Scaffolding 'real-world' apps

You can use `Truss` to generate a pure client side (Polymer) app, or you can
scaffold an app with a server-side component, or a persistence layer.
It's early still (there's little more than this README at this time), but
given the 'Blog' data structure described above, you should be able to
use `Truss` to generate the following Polymer apps:

- with AppEngine and DataStore
- with Rails and MongoDB
- with Flash and MySQL

