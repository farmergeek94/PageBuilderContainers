Restores Kentico "Webpart Containers" to MVC Page Builder Widgets.

This package is for Kentico 12 SP, to be installed on the MVC web application and not the Kentico Application ("Mother").

# Installation
## Part 1 - Kentico Application ("Mother"):

1. Install `PageBuilderContainers.Kentico` Nuget Package on your Kentico Application
1. Rebuild your web application
1. Log into Kentico as a Global Administrator
1. Go to Modules
1. Search and edit `Page Builder Containers`
1. Go to `Sites` and add to your site.

## Part 2 - MVC Site

1. Install the `PageBuilderContainers.Kentico.MVC` NuGet package on your MVC Site and rebuild

## Part 3 - Add to Widgets
1. Have your Widget Properties Model class inherit from `PageBuilderContainers.PageBuilderWidgetProperties`
1. In your Widget's View, add `@Html.PageBuilderContainerBefore(Model)` at the beginning of your rendering, and `@Html.PageBuilderContainerAfter(Model)` at the end
- Note: "Model" must be the Widget Property Class object, if using a model of `ComponentViewModel<YourWidgetModelClass>`, then your property may be `Model.Properties` instead of `Model`

# Usage
## Create Containers
1. Go to the Page Builder Containers UI element in Kentico
1. Create your Containers or edit existing. 
1. You can use `{% ContainerTitle %}`, `{% ContainerCSSClass %}`, and `{% ContainerCustomContent %}` as part of the default Container Properties

## Add Widget and configure Container
1. Add your widget to a Page Builder Area in Kentico, you will see the Containers Name, Title, CSS Class, and Custom Content properties in the Widget's configuration dialog (cogwheel icon)

# Contributions, but fixes and License
Feel free to Fork and submit pull requests to contribute.

You can submit bugs through the issue list and i will get to them as soon as i can, unless you want to fix it yourself and submit a pull request!

This is free to use and modify!

# Compatability
Can be used on any Kentico 12 SP site (hotfix 29 or above).
