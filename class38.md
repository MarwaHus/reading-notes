# Class 38

#### What are the three criteria an acticity’s intent filter must fulfill in order for a system to send an intent to that activity?
The three criteria an activity's intent filter must fulfill in order for a system to send an intent to that activity are as follows:

1. Action: The intent filter must specify the action that the activity can perform. An action is a string that describes the specific action or behavior that the activity expects to receive. For example, an activity may specify an action such as "android.intent.action.VIEW" to indicate that it can handle the viewing of data.

2. Category: The intent filter may optionally specify one or more categories that the activity belongs to. Categories can help the system to narrow down the set of activities that can respond to an intent. For example, an activity can specify the category "android.intent.category.DEFAULT" to indicate that it is a default choice for the given action.

3. Data: The intent filter may also include one or more data elements that describe the data type or URI scheme that the activity can handle. This allows the system to match the intent to activities that can handle the specific data. For example, an activity that can handle image files may specify a data element with the MIME type "image/*" to indicate its capability.


#### How does an activity retrieve the Intent that it was started by?
In Android, an activity can retrieve the Intent that started it by using the <b>getIntent()</b> method. This method is part of the Activity class and returns the Intent that started the activity.


#### Explain intents to a non-technical friend.
Intents are like messages that apps on your phone can send to each other. They allow apps to ask each other to perform specific tasks, like sharing a photo from one app to another. The intent contains information about the photo and what the receiving app should do with it. The Android system helps match the intent with apps that can handle it, and you can choose the app you want. Intents make apps work together easily, allowing them to communicate, share data, and trigger actions, improving your phone experience.

#### Compare and contrast implicit and explicit intents.
Implicit Intents:
- Implicit intents are used when you want the system to find and start a suitable app to handle a specific action without explicitly specifying the target app.
- You provide a general action for the intent, such as "share" or "view," and the system looks for apps that can handle that action.
- The receiving app is not predetermined – it is determined dynamically at runtime based on the available apps that can handle the intent's action.
- Implicit intents are helpful when you want to give the user options and let them choose which app to use.
- They are more flexible because multiple apps can handle the same action, giving the user the freedom to choose their preferred app.

Explicit Intents:
- Explicit intents are used when you want to specifically target a particular app to handle an action.
- You explicitly specify the component (activity, service) or the package name of the target app that should receive the intent.
- With explicit intents, you directly specify the app and the specific behavior you want to trigger.
- These intents are useful when you know in advance which app should handle the intent and want to ensure that a particular app is always used.
- Explicit intents are also commonly used within an app to navigate between different screens or trigger specific operations.


#### What is the primary information contained within an Intent?
1. Action: It specifies the general type of operation or action that should be performed, such as "send" or "view."

2. Data: It represents the data or content to be used or acted upon, such as a URI pointing to a specific file or a location on the web.

3. Extras: These are additional pieces of data, such as key-value pairs, that can be passed along with the intent. Extras provide more specific information related to the action or data, like a caption for an image or a subject for an email.

4. Categories: It defines additional categories or attributes that describe the intended action or the types of components that can handle the intent.

5. Component: In the case of an explicit intent, it specifies the specific component (e.g., activity, service) within an app that should receive the intent.