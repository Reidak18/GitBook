# Demo scene: 1 - Play Animation

Demo scene is located in the Easy Lip Sync/Examples folder. Let's look at runtime scripts used to play animation.

### Universal Player

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption><p>UniversalPlayer</p></figcaption></figure>

Attached to AudioSource GameObject. This script is a wrapper for the Unity AudioSource component and allows you to get the percentage and absolute playback time of audio to sync with lip animations.

### AudioSyncAnimator

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption><p>AudioSyncAnimator</p></figcaption></figure>

Attached to Matilda GameObject. This script is used to synchronize speech playback with lip animation. Required the UniversalPlayer and an index of the animator layer with lip sync animation.

### EyesController

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption><p>EyesController</p></figcaption></figure>

Attached to Matilda GameObject. This script is used to direct the eyes to an object (camera in the demo scene). Required the target object, left and right eye transform and the speed of their rotation. Please note that your avatar model may be different from Matilda's and will require changes to this script to work correctly
