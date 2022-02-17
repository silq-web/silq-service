# SILK

**S**ilk **I**s **L**inked **K**nowledge

- Service for creating semantically linked documents and records with rich content

- documents are markdown extended text files which can compile into pdfs, web pages, or other views

- documents can have rich media insertion

- Records can be generated by document generators

- API for command line, REST, Web Sockets and SMS; real time?

- graph model of data with underlying SQL DB

- allow for math, plantUML?

## stack

- Node w typescript
- graphql + postgres

## object types

document

document generator

record

tag

*user*

## collection types

document files

document library

record set

document generator library

*collaborators*

## api scopes

document:create

document:archive

document:unarchive

document:edit

document:share

document:unshare

document:get

document:get_files

document:get_all

document_library:create

document_library:edit

document_library:archive

document_library:unarchive

document_library:get_documents

document_library:share

document_library:unshare

document_library:add_documents

document_library:remove_documents 

document generator:create

document generator:update

document generator:archive

document generator:get

document generator:get_records

document_generator_library:create

document_generator_library:edit

document_generator_library:archive

document_generator_library:unarchive

document_generator_library:get_generators

document_generator_library:share

document_generator_library:unshare

document_generator_library:add_generators

document_generator_library:remove_generators

record:get

record:get_files

record:copy_to_document

record:share

record:unshare

record:archive

record_set:get

record_set:share

record_set:unshare

record_set:archive

record_set:unarchive

tag:get_documents

tag:get_all

## document

metadata

- id
- date created
- date edited
- immutable document history
- creator
- *privacy*
  - *public*
  - *shared with*
  - *hidden from*

markdown compliant text file

associated empheral file system; flat

markdown superset syntax

- `#<text>` - bi-drectional graph link; link documents together via shared tags
- *`@<text>` - tag another user available to you; automatically adds view permissions to that user*
- `{{name, type}}` - placeholder for file or linked document
  - on saving file, prompted to enter location of file content for each placeholder, which is then linked via markdown
- ontological tag....

## document generator

templating system for generation of records

*forkable by friends, current user*

incremental versioning of generator

metadata

- id
- date created
- date edited
- immutable document generator history
- forked from
- version
- creator
- *privacy*
  - *public*
  - *shared with*
  - *hidden from*

markdown superset syntax

- `[[name, type]]` - content prompt; must have unique name. types include text, file, or nested document generator
  - careful to avoid infinite loops here

generates a record, which is also a document 

## records

generated by a document generator

records store in progress data until completed, even asynchronously

metadata

- id
- date created
- fileld by id
- *privacy*
  - *public*
  - *shared with*
  - *hidden from*
- document generator id and version


immutable, but can be cloned into a document but loses all provenance to record