# User Permissions and Accessibility

_From: The chairs and members of the [Accessibility Platform Architectures Working Group (APA)](https://www.w3.org/WAI/APA/)._

In our cross-W3C scope, we work to ensure that all W3C published specifications provide support for accessibility to people with disabilities (PwD). Among our members are PwDs including people who are blind, vision impaired, deaf, hearing impaired, or have cognitive or learning disabilities.

User permissions, to us, embraces many digital activities that concern us deeply, such as the usability of authorization (AuthZ) and authentication (AuthN) interfaces and the need for accommodations such as assistive technology. PwDs have always strongly objected to automated disclosure of their disability status on the web. This information is deemed highly personal and irrelevant in most online situations. Furthermore, having experienced various forms of discrimination in the physical world, PwDs yearn for an equal opportunity in the virtual world of the web.  We offer two main examples...

## CAPTCHA

While many treat CAPTCHA as an irritating speed bump on the internet highway,  CAPTCHA can literally prevent a PwD from accessing a resource. For example, asking users who are blind, visually impaired or dyslexic to identify textual characters in a distorted graphic is asking them to perform a task they are intrinsically least able to accomplish. Similarly, asking users who are deaf, hard of hearing, or living with auditory processing disorder to identify and transcribe in writing the content of an audio CAPTCHA is asking them to perform a task they’re intrinsically least likely to accomplish (see <https://www.w3.org/TR/turingtest/>). We see a way out in relatively new Webauthn and FIDO authN schemes.

## User Preferences

For many, user preferences such as dark mode are helpful features that make consuming internet content more comfortable. They don't mind revealing these preferences, as preferring "dark mode" doesn't say anything about the person requesting the enhancement. For PwDs, user preferences are not nice-to-have; they are essential. That said, they are too revealing. Yet disclosing disability-related accommodation needs can serve as a powerful vector to getting such accommodation support. Consider that a person who is blind, using a screen reader, does not need a light or dark mode toggle, and a deaf person does not need a volume control; yet neither of these people may wish to share the fact that they are disabled. We see a way out in relatively new privacy-preserving verifiable credentials.

The two examples above are brought to highlight the contradiction at the heart of many PwDs' digital experience. On the one hand, PwDs require accommodations to access the experience, and would love for these accommodations to accompany them to every app, web page and voice assistant. On the other hand, PwDs do not want accommodations or their use of assistive technology to reveal their disability, or to define them.

## Use cases for novel technologies

APA is excited to find in the growing maturity of recent novel APIs and innovations such as Verifiable Credentials, Digital Identifiers and Webauthn the potential to find solutions to these challenges. We see the following as offering very real improvements to the lives of PwD:

* The ability to prove we are human, without being forced into tasks we are least able to accomplish (see <https://www.w3.org/TR/turingtest/>).

* The ability to login to a federated environment without a password, and perform multi-factor authentication with sufficient time to complete the task.

* The ability to selectively disclose needs for accommodation without revealing any personally identifiable or correlatable information.

* The ability to digitally enable another person to perform certain actions on one's behalf.

* The ability for a user agent to mediate on-the-fly and render services in ways that are more appropriate for people with specific accessibility needs.

* The ability to progressively trust commercial, medical, and legal providers, and enable the sharing of more information as a relationship develops, or to cut off access should a relationship need to end (see <https://www.w3.org/WAI/APA/task-forces/research-questions/wiki/Some_use_cases_for_verifiable_credentials>).

## Terms of service

Terms of Service, and their general level of complexity, pose a significant barrier to most of us in understanding their implications. This is exacerbated for people who face additional cognitive accessibility barriers. Simplifying these would benefit all people using the web. Community-sourced extensions such as [Terms of Service: Didn't Read](https://tosdr.org/) aim to provide a quick indication of how user-friendly the terms on certain sites are.

## Fingerprinting of assistive technologies delivered via browser extensions

Assistive technologies may be (and several are) delivered via browser extensions that modify the page in order to make the content more accessible/usable by PwDs (e.g. [Chrome accessibility extensions](https://chrome.google.com/webstore/category/collection/3p_accessibility_extensions)). There is an inherent fingerprinting/privacy risk, in that a page, could detect changes being made, by way of the MutationObserver and other general DOM APIs, and infer which extension making those changes. Whilst this would involve a lot of effort to implement, it is possible, and therefore it is a risk, particularly in relation to bad actors.

Part of the solution to this issue may be to allow browser extensions to request that the browser _not_ fire DOM mutation events for changes made by the extension. Whilst that would not eliminate all possible fingerprinting vectors, it would create a major block on fingerprinting possibilities. Further investigation and discussion is needed. Of course this also applies to extensions for everyone that simply seek to improve the usability of pages.

## Next steps

We look forward to bringing our experience in cross-W3C specification review to considering the side variety of Web APIs that will be discussed in this workshop. We are eager to engage with the gathered experts from every discipline and ensure that all these diverse professionals are hearing the voices of PwDs.
