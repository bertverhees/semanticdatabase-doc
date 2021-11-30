# Semantic Database

Data should be accompanied by semantic explanation, only in this way can be searched and can be found.

The design principles should be simple, the possibilities to use it should be endless

I'm building a simple infrastructure that I call "semantic database". For now it is a hobby project, just for fun.

## OpenEhr

OpenEhr is an semantic database design with a single Reference Model for a single purpose. It is where this idea comes from. It is one of the giants on which shoulders I am sitting.

It will consist of several parts:

## [The Reference Model](https://github.com/bertverhees/semanticdatabase-rm)

The Reference Model is a generic model which allows archetypes to refer to. For example, the OpenEhr Reference Model, mainly consist in a few classes which give a main-structure to model clinical based archetypes. Clinical matters are based on a few generic main-classes: Observation, Evaluation, Instruction, Activity. In a single patient-case, these classes can be combined in a Composition. For example, a patient with a disease will be diagnosed, and after that (mostly) action will be taken.

From these classes a wide variety of data can be described. For example, for observation, temperature can be measured, or blood-pressure, that are different data-constellations, but they will be stored as Observation.

So in the OpenEhr Reference Model, there is an Observation-class which can store many different data-constellations. The constellations are described in Archetypes, so there are archetypes for temperature and for blood-pressure. The archetype takes care for the semantic explanation of the data. The data always carry as property the name of the archetype which describes them.

Data are not shatterd around, but accessible in a group, having the description and context, and because the are in compositions, the have other Reference Model-classes tot extend the context.

For understanding we can say that Archetypes are specialized classes for the generic Reference Model

How the Reference Model is build, how it is communicated, and checked, that is described in the documents accompaning the Git-project which is linked in the header.

## The Archetype Model

## The Archetype-based Query Tool

## The Archetype-based Database
