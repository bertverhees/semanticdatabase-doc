# Semantic Database

##[Semantics](https://en.wikipedia.org/wiki/Semantics)
Semantic data stand for data is referencing to meaning and context:

For example, the color Red: 
Red has a complete other meaning in another context. For example, there is a political color red, there is alizarin red, an oil-paint pigment/color, red states in the US are republican dominated states, but red countries are communist countries. Redskin is disrespectful slang for native Americans, while red skin can indicate seborrheic dermatitis.
On a banc-account, red stands for depts and in romantic communication red stands for warmth and love, in your car, on the dashboard-gauges, mostly they indicate a critical situation.

To understand data, the context must be known. That is what the semantic database provides, context and meaning.

The design principles should be simple, the possibilities to use it should be endless

For now it is a hobby project, just for fun.

#### OpenEhr

OpenEhr is an semantic database design with a single Reference Model for a single but large purpose (healthcare). The semantic-database-concept is a widening of the OpenEhr idea. It is making semantic-storage possible for many domains, in fact, all domains.

## Overview

![](overview.png)

quick and dirty drawing ;-)

#### The Reference Model

This contains classes needed to be the base of archetypes or being used in archetypes.
We will always need datavalues like text, number, quantity, date-time and data-structures like list or set or table
Besides these we can choose to have domain-classes, these are the base of archetypes, but these can also be omitted and data-structures being used instead.

OpenEhr has a few domain-classes in their reference model, they decided that healthcare semantics needs a few fixed base-classes, for example Observation, Activity, Evaluation, Instruction, but also which comes handy, demographic classes.
There is nothing wrong with that but it narrows the interoperability to other ideas. One of the goals of the semantic database is to support constructs like OpenEhr.
But it will also support the EN13606 Reference Model which also has domain-classes but other, and FHIR which has HL7 related. So many ways, in healthcare only. All these different concepts can be stored in one single database.

But the semantic database will also support, for example, taxonomy in different disciplines, natural sciences, business and economics, computing, military, research taxonomy, astronomy, even astrology.
It will support a databases for a small business, a grocery or a hardware-store, accounting-software, hotel, kindergarten, I cannot think of a purpose which it cannot support.

All thinkable purposes, even in one database, distributed, cloud, local, no creation of tables, just write your archetypes and you are in

All data are, if done right, self-explanatory, no unclear relationships or tables, no foreign keys, no cryptic fieldnames

#### The archetypes

The archetypes are kind of descriptive data-definitions, they contain information about who wrote them, why, they explain the data-items, the context, the purpose, the cardinality, the occurrences.

They are build on base of as such designated domain-classes, demography-classes, or datastructure classes. As to say, they are a constraint, restriction on those base-classes

Those classes have properties which are datavalues, datastructures or, if the reference model allows, other domain classes.

All datasets that go into the storage have an archetype-identifier as field, so the reference to the descriptive archetype is always present. There will be no data in the database without this field. All datasets are validated against the archetype.

#### The Database

The database is a document database with a data-oriented data-process-layer.

#### The Query Engine

The query engine allows to query on documents. It can use indexes to often used data-items. The queries are based on archetype-id's and paths inside archetypes

## [The Reference Model](https://github.com/bertverhees/semanticdatabase-rm)

## The Archetype Model

## The Archetype-based Query Tool

## The Archetype-based Database
