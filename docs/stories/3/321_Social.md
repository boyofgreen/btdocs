# Task 3.2.1 - Support sharing images to Social Networks

Our users want to be able to share images to their social networks. We want users to spread the word for our products. Enabling the application to share content on every platform will make everyone happy.

## Prerequisites 

This task has a dependency on [Task 3.1.2](312_Camera.md) and all of it's prerequisites

## Task

1. Support sharing content through each platform native share integration
2. Support sharing to Facebook or Twitter directly from the app (min UWP)

## Comments

###### @ 9:23am
We can use the same method as in [Task 3.1.2](312_Camera.md) to create a sharing class for every platform. Found [this blog](https://xamarinhelp.com/share-dialog-xamarin-forms/) post that does something similar.

###### @ 10:31am
We can use the UWP Community toolkit to share to [Facebook](http://docs.uwpcommunitytoolkit.com/en/master/services/Facebook/) and/or [Twitter](http://docs.uwpcommunitytoolkit.com/en/master/services/Twitter/) directly on UWP. Sharing to facebook seems super easy:

```csharp
// Initialize service
FacebookService.Instance.Initialize("AppID");

// Login to Facebook
if (!await FacebookService.Instance.LoginAsync())
{
    return;
}

// Post a message with a picture on your wall
await FacebookService.Instance.PostPictureToFeedAsync("Title", picture.Name, stream);
```

## continue to [next task >> ](322_Rome.md)




