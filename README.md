# PAN-OS Config Elements

XML-based config skillets for NGFW and Panorama. 

Prototyping the tech library concept to use with caution. Names may change.


## Config snippet grouping under ngfw 

 * common file: capture all vars and snippets; must reference at snippet layer
 * snippet groups: capture reference config groups used in combination with
 add on items in separate files
 * snippet groups granular: try to break all config elements into unique files
 with one or a few snippets
 
 The sample_skillet_playlists dir shows how these would be referenced.
 
### Common File option

This can be used for random groupings of content but not recommended to replace
snippet groups. In this example there we had issues with re-use of variables and
how sourced. You also require the user to have knowledge of how items are
 grouped since this is not designed as a 'play all' file.
 
 So less solution / use case oriented and more about a way to dump in a bunch
 of snippets without combining through multiple files.
 
 ### Snippet Groups
 
 This provides for a mix of use case 'ready to load' components in tandem with
 a set of add-on/optional elements.
 
 In the network example you can pull in 2-interface/zone L3, a vwire, or
 L3 mode with multiple L2 phy interfaces. These work as a complete set including
 interfaces, zones, virtual routing, and interface mgmt profiles.
 
 So use case specific snippet groups.
 
 DHCP server and NAT become more optional and not included in the base network
 configuration.
 
 The 'includes' playlist would grab a base topology config and then include 
 these additional add-on components.
 
> NOTE: Most of the snippet grouping will use a common set of variable names
> that span the various snippets. This simplifies variable name re-use
 
 ### Snippet Groups - Granular
 
This is very similar to the snippet groups option yet tries to be more granular
with common re-used elements. In the network example the interface mgmt
 profiles, base virtual router configuration, and internet vs internal L3 pieces
 are broke out into separate files.
 
This works to have more 'mix-and-match' capability without replication of common
elements yet requires the user to levarage includes playlists to put the pieces 
together in a useful way. This becomes similar to the common file model breaking
quick reference config snippet groups.

The other challenge is ensuring that all of the granular components know to
re-use key variable values referenced all use case configurations.


