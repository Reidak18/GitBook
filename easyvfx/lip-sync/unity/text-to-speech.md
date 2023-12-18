# Text to speech

The plugin provides tools for synthesizing speech from text.

When synthesizing, there are several voice synthesis providers available below. The list is to be expanded in the future.

Available voice providers for use:

<table data-header-hidden><thead><tr><th width="198.5"></th><th></th></tr></thead><tbody><tr><td>Engine ID</td><td>Voice ID</td></tr><tr><td>google</td><td>https://cloud.google.com/text-to-speech/docs/voices</td></tr><tr><td>azure</td><td>https://docs.microsoft.com/en-us/azure/cognitive-services/speech-service/language-support?tabs=stt-tts</td></tr></tbody></table>

VoiceID male and female are also available for all engines as default synonyms for voices.

To use the TTS option from the editor and generate a sound asset go to **Tools -> Easy Lip Sync -> Create Speech from Text**.

<figure><img src="../../../.gitbook/assets/Screenshot 2023-12-07 at 15.12.16.png" alt=""><figcaption><p><strong>Create Speech from Text in Unity Editor</strong></p></figcaption></figure>

<figure><img src="https://lh6.googleusercontent.com/3dFP-dfg4pXODNLNXgadatornUcosCgVm28bCmGAHH5Zqn8ABVQZsIHRneGPNpaJdaW4BQAVQkhJ8Lq016mbbFrshe_wwuCAJHfaHtZOoTz314z0WxOixNHh7FrIC-6vACw7NukiC-XpxUfipHQEpys" alt=""><figcaption><p><strong>Create Speech from Text in Unity Editor</strong></p></figcaption></figure>

The ​​generation window pops up on the screen. Here you need to fill in the **TTS Engine** and **Voice ID** fields with the values from the table above. In the **Text** field enter the phrase to be voiced. You can also create a lip-sync animation right there.

**Attention:** You should select the voice id value corresponding to the language of your text phrase. Choosing the incorrect language can affect the quality of tts.

<figure><img src="https://lh6.googleusercontent.com/vNzq-mM5tGIT_V4Ln5vwwXOqs8fcFqHqLfV8VHKSS585DFWYcrGGG6rHeYjbo_Ik0HD0RXXrQW-YS4oPjDBPk9r1JqhKK1agxJK9Bz2a8eS8YhrKtCPsEJJ0rlbLx8L8qz9EB-ouNNsAlIIGafjYa00" alt=""><figcaption><p><strong>Create Speech from Text window</strong></p></figcaption></figure>

Press the **Generate** button. After receiving the results, select a folder to save the wav file.
