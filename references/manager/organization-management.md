---
description: 'On this section, you will find information about organization management.'
---

# Organization management

Here you can see on the platform all the organizations you have created. Besides that, you can manage your organization's token or to make a permission management of your users. 

###  Organization's token 

The token is a resource you can create to use in your analysis. The main goal is to help Horusec identify the organization and the repository when the [**CLI** ](../cli.md)sends a new analysis to the platform. 

For example, if you create an organization with 100 repositories, you will need only 1 access token. At the moment you send an analyis to this repository, you will have to pass the repository's name that you want to create or it already exists to the CLI. 

Despite you have the option to create the token, it is safer to generate only one token to the repository and revoke it after a while. This way, you make sure the organization will always be safe. 

{% hint style="danger" %}
Remember when creating an access token, it only be seen once.
{% endhint %}

You can see how the token dashboard is in Horusec: 

![](../../.gitbook/assets/tokenen_us.gif)

### Organization's users

You can invite new users to enter your organization. To do that, you have do register them in Horusec's database and at the end of the process, an email is sent to invite the users to enter that organization. 

When you invite, you have to choose the user's function inside the organization. There are two main funtions, each one has the following permissions:

1. **Manager**

   * Manage the organization \(view, update, remove\);
   * Manage organization's tokens \(create, view, update, remove\);
   * Manage organization's users \(invite, view, update, remove;
   * Add new repositories;
   * View all the repositories in the organization;
   * View the organization's dashboard;
   * Visualizar repositories' dashboard the user has access to.

2. **User**

   * View repositories' dashboard the user has access to. 

![Page to manage the users of your organization](../../.gitbook/assets/usuariodeorgaen_us.gif)

