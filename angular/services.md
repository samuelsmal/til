---
tags: angular, service, factory, provider
created_on: 2016-02-22
updated_on: 2016-02-22
---

Quoted from
[stackoverflow](http://stackoverflow.com/questions/16565105/when-creating-service-method-whats-the-difference-between-module-service-and-mo)
which got it from a [Google
Group](https://groups.google.com/forum/#!msg/angular/hVrkvaHGOfc/idEaEctreMYJ):

In fact `$provide.provider`, `$provide.factory` and `$provide.service` are more or
less the same thing in the sense that all of them are blueprints / instructions
for creating object instances (those instances are then ready to be injected
into collaborators).

`$provide.provider` is the most sophisticated method of registering blueprints,
it allows you to have a complex creation function and configuration options.

`$provide.factory` is a simplified version of `$provide.provider` when you don't
need to support configuration options but still want to have a more
sophisticated creation logic.

`$provide.service` is for cases where the whole creation logic boils down to
invoking a constructor function.
