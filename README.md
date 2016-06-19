# Structured and hyperlinked edition of Spinoza’s *Ethica*, using Commonmark embedded in TOML

This is still at a very early stage, and not ready for any kind of usage.

## Status:

- Latin (Gebhardt): In progress (part 1 over, part 2 in progress)
- English (?): In project
- French (Appuhn): In project
- Chinese (?): In project

## Scripts

A collection of scripts will be written to render the book in multiple formats, including html. Translation to portable sql should also be possible.

## Format

The Ethica is represented as a nested dictionary, with paths of the form
`[type.number.type.number]`. For example, `[pars.1.prop.16]` is the path to part 1, proposition 16.

In each content node, a `txt` field contains the text, and a `refs` holds the references for hypertext. References in the text follow the commonmark link specification.

Internal links may be specified by using the path of the desired node, like `pars.1.def.3` for part 1, definition 3.

A special field will be used for ordering (needed for example in part 2).

### Why not markdown?

Although some flavors of markdown, like pandoc’s, have per-block metadata and other advanced features, they do not have the same expressive power as toml.

### With embedded markdown strings, don't we loose the tooling around plain markdown?

As the metadata should migrate into toml, the embedded markdown is little more than plain text. And what is lost in markdown tooling is gained in toml tooling.

## Acknowledgments

The latin text is from [ethicadb](http://ethicadb.org).

## Contributions

are welcome.

## License

Spinoza’s work is in the public domain. Any part of this repository where copyright is applicable is released under the GNU Public License version 3 or later. By contributing to this repository, you accept that your contribution be attributed the same license.

*Copyright 2016 Tom Houlé and contributors*
