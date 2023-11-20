# Apply to avatar

You can apply the generated lip sync animation to the example avatar.&#x20;

Open the demo scene from **Easy Lip Sync/Examples/1 - Play Animation**.&#x20;

<figure><img src="https://lh4.googleusercontent.com/XEJAolJYQriz-_OWn-3zoSM0z0lOaw2Zi-WjLcpaDzWUN-KcRPjD2gq_4CPiw911MbI4xkMR5h5FVZYjIEZPOBp8KRvLs-JWd4GF-fb8AehTRkF_4DE6oCsXVach2ALIU8lsIsHtVY32TOK8aN_tN28" alt=""><figcaption><p><strong>1 - Play Animation scene in the Assets folder</strong></p></figcaption></figure>

Choose the **Audio Source GameObject** in scene hierarchy and set your .wav file in **AudioClip** field in **Audio Source component**.

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption><p>Audio Source GameObject in the scene hierarchy</p></figcaption></figure>

<figure><img src="https://lh5.googleusercontent.com/S6MZ1qvTNV9v2TBdhdLsHCw6GEPinzP_-XrDzyqm3qN6g67yIzi-jVf_JWZ2Udbmo51WIf7uJCQCujoGioR9W414MEpYyGte5W4iaKzf4Ne4YoMUJw1w-EfIbiknhqa7TH3MIxYKm5_UuL7_vnpb6II" alt=""><figcaption><p>The audio source component on the Audio Source GameObject</p></figcaption></figure>

You can use generated animation as default unity animation.&#x20;

For this you should create an **Animator Controller**. Right click in the Assets folder in the project window and in the context menu choose **Create -> Animator Controller**. Enter any convenient name.

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption><p>Creating an Animator Controller from context menu</p></figcaption></figure>

Select created Animator Controller and go to **Window -> Animation -> Animator**.

<figure><img src="https://lh5.googleusercontent.com/7j9PUgQAq8CtBCjlmt6fcOYhvk_PEyUTkBC8CBFJPJbvNNMXXwRDAFJQQMzmAzHaQ4Y0j2la3rDNPuwnWeGBnve8qiKG5-8tBquqsqPfi6OXRrZDsc9KCtY_RIJft67F9Z5XC0BNiykO2Eu0dkxndtw" alt=""><figcaption><p>Open the Animator window</p></figcaption></figure>

Please note that in Layers > Base Layer > Blending you should have a function called Override, not Additive.

Drag and drop your generated animation file (phrase.anim) into the opened window. Arrow from the Entry block to your animation will be created automatically.

<figure><img src="https://lh4.googleusercontent.com/2V9GIzZ0YTexBb-fRR_LHyRfH2DfUwz1OxKqOPQdAZrd590YfsG18yc6_fQuCCSSvoKnQsh2o87q4mX7pPd8Bp3C3CRmzQQpvFSyHZyYldY9vYDs-94RIw6s4EpbS7ImEtVYJMqiL9SOHvpvhSiD0EU" alt=""><figcaption><p>Add the generated lip sync animation in the Animator Controller</p></figcaption></figure>

Next step is to go back to the Scene window, choose the **Matilda** GameObject in the scene hierarchy and set the created Animator Controller in the Controller field in the Animator component.

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption><p>Matilda GameObject in the scene hierarchy</p></figcaption></figure>

<figure><img src="https://lh6.googleusercontent.com/GlFuhMHr0I6X1JNRj_C3Cwnm205iXmOURCqdYmTWYOCGkG8MzbxNfPX7xvh1v-aLXYDGc5_f3yc3XsOWKln39EGa32IXAl9DSry5NmictTU5ARrQaRyGKOIGMQpwizJRxup8GC_F4Gwi_qDrhYZf2Qc" alt=""><figcaption><p>The Animator Component on the Matilda GameObject</p></figcaption></figure>

Then you can run **1 - Play Animation** scene. The speech and the animation will be played.
