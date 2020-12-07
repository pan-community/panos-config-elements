# Playlist Comparisons

## common

This shows explicit reference to snippets and variables.

Not recommended for common network use case deployments since requires the
 builder to have knowledge of all snippets and how they work together.
 
 > NOTE: this model is likely to be used in IronSkillet and other use cases
> that want to build from existing use case tech library entries

## skillet groups (not granular)

this shows a basic playlist only referencing snippet group files and not
explicit snippets or variables.

Assumes the content is created for a specific use case and easily stacked.

## skillet groups - granular

this is also using group files and not explicit snippet references. However
there is a longer list requiring the builder to work across files to get a
 solution to work when elements are referenced across files.
 
 