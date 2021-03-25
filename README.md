# README

Example of Widdershins not correctly generating example requests when there is an "anyOf"

In the example, we have the schema for a "sample" which requires a name, and any of "alpha and bravo" or "charlie and delta". The example only considers the anyOf, and ignore the required "name" property.

The issue also exists for "oneOf" but "allOf" works as I'd expect.