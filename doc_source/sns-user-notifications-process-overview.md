# User Notification Process Overview<a name="sns-user-notifications-process-overview"></a>

1. [Obtain the credentials and device token](sns-prerequisites-for-mobile-push-notifications.md) for the mobile platforms that you want to support\.

1. Use the credentials to create a platform application object \(`PlatformApplicationArn`\) usingaa Amazon SNS\. For more information, see [Create a Platform Endpoint and Manage Device Tokens](mobile-platform-endpoint.md)\.

1. Use the returned credentials to request a device token for your mobile app and device from the mobile platforms\. The token you receive represents your mobile app and device\.

1. Use the device token and the `PlatformApplicationArn` to create a platform endpoint object \(`EndpointArn`\) using Amazon SNS\. For more information, see [Create a Platform Endpoint and Manage Device Tokens](mobile-platform-endpoint.md)\.

1. Use the `EndpointArn` to publish a message to an app on a mobile device\. For more information, see [Send a Direct Message to a Mobile Device](mobile-push-send-directmobile.md) and the [Publish](https://docs.aws.amazon.com/sns/latest/api/API_Publish.html) API in the Amazon Simple Notification Service API Reference\.

1. Using the information from the mobile platforms, [publish a message to a mobile device](mobile-push-send.md)\.