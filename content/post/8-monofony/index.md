+++
title = "[EN] Monofony"
subtitle = "A Symfony project based on the internal structure of Sylius"

date = 2019-12-26
draft = false

authors = ["Gabi Udrescu"]

tags = ['en']
+++
{{% toc %}}

*Translator note: once I saw the [original article](https://afsy.fr/avent/2019/22-monofony-base-sur-la-structure-interne-de-sylius) shared on Sylius Slack, I thought it would be useful to translate it in English, as my French is not that good; this should help me in the future when someone asks me why use Monofony and why is this package that great; I also took the liberty to rewrite the original article with my own words, following the original idea.*

# The itch

My personal belief is that whenever you have an itch, there is someone out there, in the world, who has already had a similar problem and, most probably, already has a solution for that. 

And, instead of reinventing the wheel, you can use your time and energy to build on existing grounds, rather than start from scratch.

Every once in a while, I tend to have *that idea* that excites me to the point when I am able to spend a few nights working on it while still attending my day-to-day job. 

But starting a new project can be a long and tedious job. If you have a great idea you want to put out there in the wild as soon as possible to get feedback and it takes you a full day only to setup such basic functionalities, such as login, forget password or user registration, the enthusiasm will soon fade away. And who wants to do a full setup for continuous integration every single time you start something new? 

# What is Monofony?

Monofony is a Symfony application scaffold that allows you to bootstrap a modern application by leveraging Sylius bundles and components, helping you to focus more on what truly matters to your use-case, rather than on the underlying infrastructure required to power things up. 

Monofony comes at hand if you:
 - have a public facing part of your application and a backend, only for admin
 - show list of items with filters, sorting and pagination
 - require visitors to login or register on your website to be able to perform certain actions
 - send emails 
 - implement complex business logic for your items where certain states have important meaning and transitioning from one state to another triggers custom behaviour 
 - expose an HTTP RESTful API
 - care about software quality to implement automated testing (unit testing, integration testing or end to end) and static code analysis

Starting a new Symfony application with Monofony allows you to work faster by using built-in functionalities from Sylius, whether you are building a backend, an API or a full stack application. You wil save a lot of time by just creating the entities and properly configure grids and forms for them.

# Some assumptions

Most of the times, you will need to manage different kind of users:

 - administrators, who will be able to access back office 
 - and customers, who will use the public part of the application / website

These two entities come by default with Monofony.

# Concepts

Everything starts from the model: the entity. 

> LazyAssTip: I usually create entities by using [Symfony MakerBundle](https://symfony.com/doc/current/bundles/SymfonyMakerBundle/index.html).

Once you created the entities you need, their properties and their relations, you can start leveraging Monofony:

 - declare your entity as a Sylius resource for CRUD operations backend
 - create a grid for CRUD operations frontend
 - create the routing required for the grid navigation
 - add a link to the existing menu of the application as an entrypoint for admin users

## Resource

When I first learned about resources, my first question was: wtf is a resource and what's the difference between that and an entity?

Well, if you declare your entity as a resource, the SyliusResourceBundle will provide you:

 - a factory class to build your entity as you need it
 - a repository with basic methods to cover adding, removing, paginating and database retrieval
 - a controller for listing entities, showing one item, creating, updating, deleting and even 

[source](https://afsy.fr/avent/2019/22-monofony-base-sur-la-structure-interne-de-sylius)

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE3OTUxMDA3MjMsMTQwNzk1Mzk4NSwtMz
EyMTczMzA1LDk2MzMzODc4LDE4MzQ0Njk2NTUsLTU0NTUwNzky
NCwtMTkwMTg4NjM5OSwtMTk2NzMwNDk0MywtMTI2NDEzMzEyLC
0xODQxMDE5OTA5LDE2NjY5NjkzODBdfQ==
-->