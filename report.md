---
layout: home
permalink: /report
toc: true
---

## Executive Summary

* Future work should build on the key strengths of the web: safety-by-default, linkability, ephemerality, and interoperability across browsers and platforms.
* There was significant interest in non-prompt, contextual permission UIs, which are more seamlessly embedded into the user's journey, and follow the "user-push" model instead of the "developer-pull" model. This approach could allow for more intuitive user controls and better contextual integrity, promote light patterns over dark patterns, and provide user agents with better insight into user intent and inform predictive systems.
* User agents could surface – or adjust behavior based on – additional signals to support informed user choices. These signals might include purpose declarations by developers, crowd-sourced statistics, ratings or reviews, etc. Defining a purpose in a structured language could enable browsers to reframe permissions in terms of utility and potential consequences rather than technical ability, and allow independent parties to audit usage. We can [learn from P3P](https://www.w3.org/2014/privacyws/pp/Binns.pdf).
* Several areas could benefit from further user research. Examples include understanding the effectiveness of browser-owned UI that crosses the so-called [line of death](https://textslashplain.com/2017/01/14/the-line-of-death/https://textslashplain.com/2017/01/14/the-line-of-death/) to mitigate spoofing risks. Another concerns the granularity and presentation of purpose specifications, such that they provide the most transparency with the least friction to users.
* There was agreement that getting the UX of permission flows right is a core aspect of making capabilities work well, especially as more capabilities get used in web apps and on a larger variety of interconnected devices. There was a desire to incorporate discussions and considerations around UX into standardization work, for example by building a forum in which to seek UX consensus among implementers and the community.
* On shaping APIs and specifications, we identified a tension between being known-use-case driven vs. generic-purpose APIs. While the former can often allow crafting better UX, the latter enables broader innovation. In both worlds, developers need guidance and the right tooling to help them deliver on their responsibilities towards users' privacy.
* For accessibility, an important short term goal could be to provide consistent _earcons_ across browsers as non-visual indicators of capability used by websites.


## Introduction

As the web's capabilities continue to grow in power and scope, it becomes increasingly important to ensure that users and developers have a shared understanding of what any given page might be able to do. This workshop followed in the footsteps of the [2018 W3C Workshop on Permissions and User Consent](https://www.w3.org/Privacy/permissions-ws-2018/report.html), exploring the ways in which user agents expose permission decisions in the status quo, focusing on aspects of usable security and user choice. As before, the workshop prioritized discussion and had limited time for presentations. The entire second day consisted of breakout sessions, which were scheduled during the workshop itself.

This report collects some highlights from the individual sessions, based on [the raw minutes](https://docs.google.com/document/d/1chQa2ab_b3gPkk58sFr5cqLVgsdWviLgZl6b9oM3wQU/edit#heading=h.5wqvtwjr07z).


## Artifacts

### Agenda

[Agenda can be found here]({{ site.baseurl }}/schedule). Slides, when available, are linked to the corresponding agenda entry.

### Participants

In alphabetical order:

*   Aniketh Girish, IMDEA Networks | UC3M
*   Anne van Kesteren, Apple
*   Anssi Kostiainen, Intel
*   Arnout Terpstra, SURF / Tilburg University
*   Ashish Ashutosh - INSA Lyon, University of Passau
*   Balazs Engedy, Google
*   Cezary Cerekwicki, Opera Software
*   Emily Turner, the Guardian
*   Florian Jacky, Google Chrome
*   Freddy Braun - Mozilla Firefox, Berlin
*   Gergely Biczók, CrySyS Lab, Budapest Univ. of Tech. and Econ.
*   Haojian Jin, University of California, San Diego
*   Ian Clelland, Google
*   Jay Kishigami, W3C (Keio Univ.)
*   Johann Hofmann, Google Chrome
*   Lukasz Olejnik, independent researcher, fellow of Geneva Academy of International Humanitarian Law and Human rights
*   Marcos Cáceres, Apple
*   Marian Harbach, Google
*   Maxime Veit, Karlsruhe Institute of Technology
*   Mike West, Google
*   Nick Doty, Center for Democracy & Technology
*   Nicolás Peña Moreno, Google
*   Noam Rosenthal, Google
*   Primal Wijesekera, ICSI | UC Berkeley
*   Robert Deimann, University Trier
*   Sam Weiler, W3C
*   Sean Harrison, Google
*   Serena Chen, Google
*   Serge Egelman, UC Berkeley / ICSI / AppCensus
*   Sharon Polsky, Privacy & Access Council of Canada
*   Shuaishuai Liu,  CrySyS Lab, Budapest Univ. of Tech. and Econ.
*   Thomas Nguyen, Google
*   Thomas Steiner, Google
*   Wendy Seltzer, W3C
*   Yi Gu, Google


### Minutes

This document is a summary of the minutes, which are [available in their raw form](https://docs.google.com/document/d/1chQa2ab_b3gPkk58sFr5cqLVgsdWviLgZl6b9oM3wQU/edit#heading=h.5wqvtwjr07z).


## Session summaries

### Permissions & Consent

**Presenter**: Lukasz Olejnik (independent researcher, fellow of Geneva Academy of International Humanitarian Law and Human rights)

**Slides**: <https://www.w3.org/Privacy/permissions-ws-2022/papers/W3CPermissionsWorkshop22\_LukaszOlejnikSession1.pdf>

In the introductory intervention, Lukasz Olejnik explained the crucial importance of Web Permissions as a natural boundary between sensitive information sources. Rather than a tool devised for regulatory compliance (i.e. consent), it is a power given to the user. It should just work. But does it?

The discussion revealed that it is still uncertain whether users understand the implications of granting access to sensitive information to be shared with a Web origin. It's crucial to "understand this understanding" (or misunderstanding?). Permissions must not be viewed as a rubber-stamp burden placed on the user, including blaming them for the potential backfires later on. The design is an important part. This element must be dealt with strictly. It is not just a matter of web security or UX, although permission prompts, and the associated information, should be communicated to the user fairly and clearly. It's not regulatory "informed consent". However, this is fine! Permissions must not disrupt web browsing, but the addition of some friction may be helpful to make the user think a bit and consider what is happening.


### Cross-platform Comparison of Permission Models

**Presenter**: Maryam Mehrnezhad, Royal Holloway University of London

**Slides**: \[Link not yet provided\]

This session began by introducing the results of three papers: a [user study on cookie notice dialogs across platforms](https://ieeexplore.ieee.org/abstract/document/9229687) (various browsers on mobile and PC as well as mobile apps), [tracking practices and user behavior across countries](https://petsymposium.org/2022/files/papers/issue1/popets-2022-0006.pdf) (UK, Germany, France), and [mobile sensor permissions via websites and apps](https://dl.acm.org/doi/abs/10.1145/3549015.3554171). Findings include the strong prevalence of dark patterns across platforms, differences across demographics when it comes to user behavior and a perceived advantage of websites over apps, as websites can "just be closed".

The ensuing discussion focused on incentives for websites to request the minimal permission they need and reducing the number of prompts. Voiced ideas included:

*   Taking requested permissions into account for search result ranking
*   Removing explicit prompt UIs and instead focusing on contextual UIs or even removing a capability altogether. The example of the ambient light sensor was given where a binary information is now provided without a permission, which suffices for most use cases.
*   Adopting purpose specifications as they exist on Mobile OSes today
*   Providing more compact representations of privacy policies in general
*   Tying capabilities to intents that users can more easily reason about. Browsers could have built-in knowledge around what's reasonable to achieve some specific goal.
*   What works or doesn't work is likely highly contextual to a given capability and situation. For example, Firefox telemetry shows that webRTC prompts have very high accept rates and it thus seems likely that users understand such prompts. For other prompts, this is likely quite different.


### Permission Misuse & Dark Patterns

**Presenter**: Balazs Engedy, Igor Bilogrevic, Google

**Slides**: <https://www.w3.org/Privacy/permissions-ws-2022/papers/Permission-Misuse-and-Dark-Patterns.pdf>

To kick off the session, the introduction contrasted anti-patterns to dark patterns using the example of the notifications permission: prompting on page load is an anti-pattern vs. tricking the user into allowing is a dark pattern. More generally, [dark strategies](https://www.petsymposium.org/2016/files/papers/Tales_from_the_Dark_Side__Privacy_Dark_Strategies_and_Privacy_Dark_Patterns.pdf) are inverses of [Hoepman's privacy strategies](https://www.cs.ru.nl/~jhh/publications/pds-booklet.pdf), and among those, data minimization, informing the user, and meaningful controls are the most actionable for user agents to improve.

The introduction then offered some hypotheses as to why dark patterns are effective: lack of meaningful controls & choices, lack of contextual integrity developer-centric capabilities, and that users underestimate consequences. For mitigation, a three-pillar approach was proposed: empower the user, change the capability, and policy based enforcement (in this order). Cross-functional teams of usable security experts maintain the first pillar, whereas the second pillar requires collaboration with capability-specific experts. Lastly, Web Permission Predictions, a recent Chromium feature, was used to exemplify an intervention of the first pillar. The feature dynamically quietens prompts that users are very unlikely to grant, thereby cutting negative user interactions in half while not interfering with grant actions. The ultimate decision is still with the user.

Follow-up questions relating to the permission prediction feature provided a natural segue into the discussion part. The group observed that both with crowd-sourced decisions (used for model training) and per-user historical decisions (used for inference), special care must be taken to ensure these decisions are genuine, and not unduly influenced by dark patterns. One solution is to deploy prediction systems alongside anti-abuse systems, the latter mitigating (or at least filtering out decisions resulting from) dark patterns.

Permission flows on legitimate websites must not be hindered due to historical user behavior on ill-intentioned sites. Per-user signals should therefore be combined with sufficient contextual (i.e. per-site) signals. These can come from multiple sources. User agents can [crowd-source grant rates](https://research.google/pubs/pub49767/), take into account whether the site is prompting in response to a user gesture, and should strive to gain more insight into the half of the user experience that takes place in the content area, leading up to the native permission prompt (see breakout session on [embedded permission element](#novel-building-blocks-for-capability-control)). Even then, the predictive model [might not work for some sub-populations](https://ieeexplore.ieee.org/abstract/document/7958626).

User agents should do more to set user expectations regarding the consequences of the various choices (e.g. how many notifications per day they should expect after clicking "Allow"), as well as ensure that the scope of the grant has the right granularity (see breakout session on [whether origin is the right scope](#keying-permissions-to-tasks-vs-origin-vs-app)). For promise-based APIs, user agents should be thoughtful about how they resolve/reject/leave promises dangling, and balance compatibility with not leaking the automated nature of the decision to the website. If the website sets up a PermissionStatus.onchange handler, then it is reasonable to reject promises more eagerly.

We concluded the session by enumerating a few additional dark patterns, including: install-time permissions in most forms, unnecessarily bundling permissions, the "bait & switch" strategy where the website primes the user for permission A but prompts for permission B (e.g. WebUSB instead of camera), and, finally, pre-prompts to only trigger the rate-limited native permission prompts when the user is likely to accept them (which is an obvious response to user agents intervening in case of low grant rates).


### User-centric Questions & Meaningful Choices

**Presenter**: Wendy Seltzer, W3C

**Slides**: <https://docs.google.com/presentation/d/1AeUnEZJ4YhdcSw1emarmH0S2xoNWavTsFOXpDHGiomA/edit?usp=sharing>

After an opening presentation pointing out where permissions developments can improve W3C spec work – both in feature-specific Working Groups and in horizontal review – the session posed some opening questions on how we might assess and improve user understanding and options. Discussion highlighted many aspects of the standards challenge of user experience (UX).

*   In designing UX, there's tension between desire for harmonization and leaving implementation choice. Review of UX considerations in spec development might help to bridge the split.
*   "Developers are users too." Can specs provide non-normative UX guidance for implementers and developers? If we don't expect standards to be revisited as understandings change, how do we keep guidance updated?
*   Build a tighter connection between research and spec-work. Research on user understanding can inform permissions requests (and suggest against asking users futile questions), especially if research investigates current questions in spec design.
*   **Action item:** Build a forum in which to seek UX consensus among implementers and community. A spec may be "feature complete" but one or more implementers reject it for UX considerations. Participants expressed interest in a forum for official discussion and consensus-building around UX, even while normative UX design remains out of scope for spec.


### Transparency and Auditing

**Presenter**: Serge Egelman, UC Berkeley / ICSI / AppCensus

**Slides**: \[Link not yet provided\]

**Summary by**: Marian Harbach

This session began with an introduction of how to think about privacy violations: Nissenbaum's contextual integrity framework describes five aspects of data sharing that are all relevant when considering data sharing acceptability: data subject, sender, receiver, data type, and transmission principles / policy constraints. If any of these deviate from a user's expectations in a given context, they are likely to perceive a violation of their privacy. This is often caused by information asymmetry: developers not knowing what's happening with 3P code, users not knowing what code does, or platforms not knowing what hosted apps or services do.

This introduction was followed by samples of existing research. One study found that the most concerning risks related to inappropriate disclosures to social relations and/or incurring costs. People generally didn't care about annoyances or actions that could be undone or stopped, such as the phone inappropriately vibrating. Another research area concerns warning messages. If users see too many warnings they don't care about, they get habituated to clicking through, negating the warnings' effects. Finally, work on auditing Android apps reveals that privacy violations often stem from three issues: developers not knowing what 3P components do; assuming that the app store review would catch inappropriate use; as well as a general lack of awareness in developers, where they don't understand their responsibilities towards users' privacy.

During discussion, the group considered approaches to improve the situation. Providing an undo option instead of asking for permission came up as a mechanism for capabilities where the sole risk is annoyance. When it comes to improving contextual integrity, three aspects were identified as important: only prompting when strictly necessary to reduce habituation; when a prompt is necessary, present sufficient information; and introduce the ability to ensure the information provided in the prompt is sufficient and accurate. All three aspects are currently problematic on the Web with the last one being the most important in the long term: without an option to audit developers' claims, there is no incentive to provide accurate information.

The group then wondered how much developers' claims on using permissions need to be backed by legal frameworks. There was a concern that we can't wait for governmental regulation and that such regulation might negatively impact the user experience in unanticipated ways when implemented in practice, as evidenced by cookie consent banners. However, there is not necessarily a need for regulation. There could also be policies enforced by the browser, for example that certain capabilities are only accessible if data sharing attributes, such as a purpose, are defined. Supporting such a definition in a structured format would immediately allow automated auditing by independent third parties. There could also be additional policy enforcement points defined by the W3C.


### Beyond Prompts

**Presenter**: Serena Chen, Google

**Slides**: <https://docs.google.com/presentation/d/1HsDd776t_YXAcsIYzkK3_-aW5WDzsJEQ5AGqi8OoGWk/edit?usp=sharing>

The purpose of permission prompts is for detecting user intent around capabilities on the web that may be outside of typical user mental models for what the web is and is not capable of. Capabilities that are within typical user mental models for what the web can do (such as display text, images, run JavaScript, etc) do not require prompts. Capabilities outside of these mental models require a stronger signal of user intent, to better match their expectations to reality.

Currently, browsers simply ask the user to allow or deny a website a certain capability. This works well for capabilities that are easy to understand, such as camera and microphone, but quickly becomes untenable for more complex capabilities, such as web USB, fonts access, etc. Additionally, introducing too many prompts risks training users to mindlessly click through prompts, rendering them useless.

This session aimed to explore additional or alternative ways to detect user intent that were not the "yes/no" questions of current typical prompts. To spark discussion, we went through 5-6 concepts on how we might expand our toolkit:

*   Reframe permissions in terms of utility rather than technical capability
*   Show what is to be shared through user selection
*   Piggyback off existing OS mental models
*   Direct controls instead of prompting; i.e., prefer user-pull over developer-push
*   Sandbox the most risky parts of new capabilities
*   In-context triggers, such as an HTML Permission Element

In the discussion portion, there was significant interest in the idea of preferring user-push moments over developer-pull. We would need to design enough consistency in this pattern.  There was a suggestion to create a GitHub repo to explore these ideas.

There was significant discussion about a potential HTML element for permission requests. There were open questions around customisation:

*   To what extent should websites be able to customize this element? For example, to style it similarly as the rest of the website
*   To what extent should user agents control how this element is displayed? For example, to prevent misuse or spoofing.

Further discussion concerned capabilities themselves: whether capabilities currently were too broad and difficult to specify use cases for. There is value in threat modeling. We also acknowledged that spoofing and fingerprinting were problems that will remain regardless of browser UI, and are very difficult to solve. However we can still try to make this harder for malicious actors, even if we are never able to solve it completely.

We also discussed using the extensions pattern for extending web capabilities, however research has shown that people are already confused about what extensions can and cannot do, and tying extra permissions to this pattern may further muddy the waters.


### Permissions UX Across Form Factors

**Presenter**: Anssi Kostiainen, Intel

**Slides**: <https://anssiko.github.io/virtual-display/permissions-ws-2022.html> ([pdf snapshot](https://github.com/w3c/permissions-ws-2022/blob/main/papers/Permissions_UX_in_Multi-Screen_Experiences.pdf))

Multi-screen experiences refer to an emerging set of use cases where the user's workspace is composed of multiple screens, e.g. a laptop and a tablet side by side. The devices that participate in this experience are not physically connected to each other and their relative positioning may change, yet the screens are expected to work together to form a virtual screen surface that enables applications to make use of this connected space. The diversity of devices make this a good testbed for permissions UX exploration across form factors. Capabilities that enable this UX are being integrated into major operating systems and exposed to applications. Apple's Sidecar and a cross-platform open-source project Deskreen are [examples](https://anssiko.github.io/virtual-display/permissions-ws-2022.html#2) of a related product feature and a web technology-based equivalent respectively.

Permissions UX in multi-screen experiences for the web [decompose into](https://anssiko.github.io/virtual-display/permissions-ws-2022.html?f=11#5) display arrangement, display source picker, virtual display creation, and window placement. Parts of this UX flow build upon in-production UI surfaces and interaction patterns, but a cohesive UX requires in addition adaptation of existing patterns for non-desktop-browser contexts.

[Display source picker](https://anssiko.github.io/virtual-display/permissions-ws-2022.html#9) control surface is in production in major browsers popularized by the [getDisplayMedia API](https://www.w3.org/TR/screen-capture/#dom-mediadevices-getdisplaymedia) and is considered well understood by users. Window placement is addressed by the [Multi-Screen Window Placement API](https://www.w3.org/TR/window-placement/) gated by a browser prompt. The generic challenge on how to speak task-oriented context-sensitive language in prompts applies to window placement. Display arrangement and virtual display creation are currently OS-managed control surfaces with no web-facing API.

A prime example of an implicit consent mechanism is [drag and drop](https://anssiko.github.io/virtual-display/permissions-ws-2022.html#16) with an [event-based Web API](https://html.spec.whatwg.org/multipage/dnd.html). The DnD action bundles two actions into one: an object selection and target location. Furthermore, it is well understood by users, but does not scale beyond pointer-based interaction. The multi-screen experience concepts presented suggest integration with modern window manager concepts may enable a [pull-based permission flow](https://anssiko.github.io/virtual-display/permissions-ws-2022.html#23) akin to drag and drop for window placement as an alternative to [push-based prompt-gated flows](https://anssiko.github.io/virtual-display/permissions-ws-2022.html#20).

Suggested future work is to further investigate pull-based permissions models as an alternative to push-based models for web capabilities at large. To support this cross-disciplinary exploration, an open forum where to seek early UX consensus across implementers for new permissions UX would facilitate the process. As of today, cross-stakeholder UX feedback is sought too late in the design process to allow for UX-initiated design iteration without breaking changes.


### New Web Experiences and App Models

**Presenter**: Penelope McLachlan, Google

**Slides**: \[Link not yet provided\]

The web is a successful application platform, especially for desktop computing applications in productivity and creativity. However, there's more opportunity for growth.

How can we offer developers the richest possible set of capabilities for building great applications, offering the power of OS native applications, while keeping the best of the web: safety, interoperability across browsers + OSs and linkability?

Many advanced capabilities, such as the ability to register file type associations, are baseline expectations of users for applications on their OS. These are necessary capabilities for web apps to offer convenient, competitive experiences for users, but they aren't powers we would want just any website to have. Today, we have a one size fits all approach where we basically pass all responsibility on to the user & site developer.

How might we differentiate between the applications that need these kinds of capabilities and random websites that might be disrupting user browsing journeys by asking for these powers unnecessarily or even using them for abusive purposes such as fingerprinting or user data exfiltration?

It may be possible for user agents to recognize that some sites are more trustworthy than others using crowd signals. For example, what if we recognize that some sites are applications (such as a video chat app) that have certain requirements to offer user value, whereas others have no need for these capabilities.

Some of the signals we could look at include:

*   If the user has installed the site as an application, taking advantage of existing user mental models around what installed apps can do
*   Developer assertions that can be disclosed at appropriate times to the user in browser UI
*   Anonymous crowd behavioral data or user behavioral data on device on the site or similar sites
*   Ratings and reviews

Some APIs we might consider restricting to differentiated, higher trust environments:

*   Borderless/seamless modes
*   Local font access
*   Compute pressure
*   Idle detection
*   File handling
*   Multi-screen window placement

What this would mean is that not all sites would get to request access to all capabilities for users. Permission requests from non-differentiated trust sites could be automatically blocked. More trustworthy sites could gain access with less friction, for example via a single permission request for multiple APIs.

If successful, we could create a web where users are safer and less interrupted than they are today because more permission requests would be automatically declined, and where it is easier for users to use web applications because it's less likely that they will get themselves into a permission state where the application cannot function in its primary capacity. For example, many users cannot use web video chat apps if they accidentally block camera/mic permission and are unable to recover.

There are many challenges to work through with this approach. The browser should _act as the user's agent_ but knowing the user's intention is not easy. We must consider, in each API, the impact of getting it wrong.


## Breakout summaries

### Novel building blocks for capability control

**Reporter**: Serena Chen

This discussion session centered around potential in-context building blocks for permissions UI — e.g., a permissions HTML element: the pros and cons of such an element, the risks involved and what it would take to de-risk such an idea. We started by recalling two papers: [How to ask for permission](https://www.guanotronic.com/~serge/papers/hotsec12.pdf) by Felt et al, and [User-Driven Access Control](https://ieeexplore.ieee.org/document/6234415) by Roesner et al.

Applying the principles in the aforementioned papers, an in-context permissions element would be some kind of element rendered in the web content area that could either trigger a classical permission prompt, or a permission grant/deny decision. This would give developers the ability to embed permissions UX in a more contextual way for users.

Concerns discussed include abuse potential, spoofing, and crossing the Line of Death. There was a back-and-forth on whether including browser UI in the web content area would erode the difference between browser and web UI, and whether this was much worse than the status quo, since users currently confuse browser and web UI often. There was concern that putting browser UI in the web content area would also open up an avenue for spoofing, however there would be no incentive to spoof this UI because spoofs of it would not be able to change any permission states, and even if there were incentive to spoof this UI, it would be customisable enough that spoofing would be irrelevant as an attack vector anyway. There is also some existing precedent for browser UI in the web content area: Safari's paste UI, and geolocation button, for example.

Clickjacking is a significant point of potential abuse, so if we were to create such a permission element, we would need to be able to guarantee characteristics such as visual stability, opacity, visibility in the z-order, and perhaps the strings / iconography displayed in the element.

Other ways to de-risk such an element could be to have the element simply trigger the current permission prompt, which overlaps the Line of Death and is clearly browser UI. However there was concern that this extra step would likely habituate users to thoughtlessly click through permission prompts, since they have already expressed their intent to grant. Another de-risking idea is to only allow temporary, one-time grants through the in-context permission UI, and perhaps to scope the fidelity of the information shared also (for example, coarse-grain geolocation rather than specific coordinates).

Further ideas were then discussed. We could potentially use such an element to incentivise good UX (user-triggered permission prompts) and disincentivize bad UX (prompting on page load). We could also leverage previews in prompt UIs to make it clear what data is shared.


### Keying permissions to tasks vs origin vs app

**Reporter**: Balazs Engedy

The group started off by forming a shared mental model of [PWA](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps)s and installed PWAs. We clarified that we mean the "[Add to Home Screen'](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Add_to_home_screen)' feature, and contrasted it to bookmarks; and to browser extensions / add-ons. Participants highlighted the complexity of this space created by the close coexistence of multiple different app models and persistence models – both for developers and users.

We then took a deep dive into the problem statement for this session; namely that while the [origin is the security boundary](https://developer.mozilla.org/en-US/docs/Web/Security/Same-origin_policy) and permission grants are scoped to origins, multiple apps can be served from a single origin. Even in tabbed browsing mode, perceived-as-different apps can exist on different paths on the same origin. The issue is even more pronounced for installed PWAs, which have the look & feel of standalone applications, and where pre-existing user mental models from mobile platforms, where users are used to application-scoped permissions, may create confusion. A similar issue exists around granting permission to a single app from a company, versus granting it to the entire company. Acquisitions happen, and separate companies may no longer be separate.

Given the web's security model, however, where same-origin contexts can script each other synchronously and communicate behind the scenes, it was not immediately obvious to the group how we can keep the permission state for two apps (from the same origin) meaningfully separate. We acknowledged that once one app has accessed a capability, the user agent cannot technically keep it from sharing data with the other app (from the same origin).

The group observed, however, that cutting off access at the source could be workable, that is, the permission grant could be scoped to what the user perceives to be interacting with. The hypothetical example was that of an origin serving both a video-conferencing and a text editor application. If the user just clicked on a home screen shortcut to start "Video-Conferencing App", and/or the foreground window shows clear branding (name, icon) of a "Video-Conferencing App", it seems quite reasonable to allow camera/microphone access in that perceived state (after an initial permission grant). Once the user navigates this PWA to a different scope, or closes it, the user's perception of interacting with a VC app is lost and the camera access should be stopped as well.

We recognized that the reasoning above is a special case of the more general idea of scoping permissions to tasks, that is, letting an app provide assistance with the task the user is trying to accomplish, while the user is engaged with that task, but when that task ends, that is a context switch that should be accompanied by a switch to the permission state. If we make the permission grant shorter, we can task-scope permissions better. We should also ask ourselves if there are better ways to define where a task starts and ends, and whether the specs could change to better accommodate that.

Increased transparency, e.g. in the form of widely-deployed permission usage indicators, could also help address user confusion. For installed PWAs that are first-class citizens on the host platform, leaning more into OS permission management and indicators drawn by the host platform is an option. Browser vendors also need to consider the needs of users with accessibility needs, for whom visual differentiation will not be sufficient.

In the status quo, we often talk about permission grants being overly broad, but in some scenarios, they can also be overly narrow. For example, users with accessibility needs might want to set up per-origin permissions on one device, and then let those permissions propagate to selected other devices. This is important for capabilities and settings like high-readability fonts or high-contrast colors.

Changing the current permission mechanics also comes at a cost. Adding the time dimension could increase friction and could make the scenario worse than we had before. Conversely, reducing friction could increase confusion. We need to be really clear about the exact problem that needs to be solved before going into solutions.


### Prompting for purpose & permission grouping

**Reporter**: Penelope McLachlan

The goal for prompting with purpose is to move away from technical prompts towards speaking the users language and help them get things done. Certain types of apps need consistent permission groupings, chat apps need notification access, VoIP apps need microphone access, video chat needs camera & mic, gaming might need USB for controllers, wake lock etc. This is a similar idea to the camera/mic grouped permission which is already shipped in Chrome but extended to more permission types.

The group had a mixed opinion on whether the approach would be declarative via the manifest (inherently untrusted) or derived by the browser (how would this work on new sites?).  There were concerns that creating predefined groups might have a chilling effect, working against novel new types of applications, or lend towards apps simply declaring themselves to be "super apps" that need all permissions

The browser cannot really vet the actual purpose of the site, it will be up to the user ultimately to determine if the use of the site is what is disclosed. It seems worthwhile to do UXR on UI disclosing the name from the manifest, an intended purpose and the set of normal permissions associated with that app in a single dialog, what is user sentiment about this UI? What changes about their behavior? Do they want to be able to selectively choose within the predefined lists?


### Accessibility considerations

**Reporter**: Janina Sajka

We discussed a range of opportunities the APA-WG is interested in developing with Privacy and Security WGs in W3C. Most especially we're strongly in support of the notion that user agents can significantly enhance accessibility by becoming ever smarter agents on behalf of their users.

Short term objectives include propagating configuration options across all of a user's various devices, so that a preference can be set once and the technology can see to it that the setting is activated on the user's other devices. We would prefer this to the too frequent situation today where configuration options need to be specified individually device by device.

Now that we're on the verge of passwordless user authentication, we should also dispose of CAPTCHA. If we can authenticate a particular human for some resource, that should suffice to authenticate that user for any resource seeking to lock out bots, but allow humans in. A particular human is always a member of the taxonomic class: Humans.

One feature that may be helpful for raising awareness of permission requests (and general notifications) amongst users of assistive technologies may be an "earcon mapping report" - it should be possible to get an index of what sound events map to which notification message, and from which app.

Longer term objectives seek to leverage privacy preserving secure digital credentials to include legal instruments such as powers of attorney which today are too often only binding as paper documents. We need these in digital form to make them more accessible to persons with disabilities, but also more readily accessible especially to medical professionals when medical emergencies arise.

We have a concern that a vicious circle can exist when a person with a disability may need to install an extension-based assistive technology, but is unable to manage permissions effectively because of accessibility barriers that may exist within the installation, or specific permission on-boarding flows until the extension is installed, and has its required permissions granted.


### Incentivizing developers to use good patterns / How to design ‘good' friction?

**Reporter**: Arnout Terpstra

First, these questions revolve around two separate target groups: developers (who are also users) and end-users (who experience good and bad friction).

For developers, being compliant with regulations is a very good reason to use good patterns: clearly specify what information they use and how they use it. However, are developers responsible for these things?

End users want to know how their data is used: who has access, for what purpose, how long, etc. In addition, trust in the party on the receiving end is crucial.

Privacy policies are currently the place where organizations specify which data they need and how they use it, however, we all know nobody reads those and they are way too long and too complicated to understand. So the question is: how do people make decisions (and what do they need to make a decision) and what kind of decisions would we want them take: how often, how granular?

An example of 'good' friction: the pin code reminder in the Signal app. Not very annoying, appears once every few weeks (with longer intervals if you get it right).

Another idea that came up: permission reports/dashboard in the browser, for instance, "this site accessed this capability for 290 of 300 minutes of being open and requested but did not use MIDI". Or visualize how data can be inferred from already shared data? Might be a bit too confronting, but it *is* reality: good friction?

Apart from reminders and other visualizations, more granular decisions are likely needed as well. Why not let the user choose "share location only once", "for 24 hours", "for 1 year"? (And regularly remind the user of given permissions). Also, technically prevent sites from getting data in for instance background / inactive tabs. Should not be possible.

So to sum up, I guess 3 important things:

1. Make some things technically impossible

2. Give users meaningful control (finding the right balance between too much and too little decisions is important!)

3. Increase transparency, remind users regularly about what they did in the past (without forcing the user to go through something if they do not wish to at that time)


### How to involve UX more in standards processes?

**Reporter**: Anne van Kesteren

The main takeaways from this session were:

*   The best standards start with use cases and end user stories.
*   People writing standards tend to shy away from UX as they don't want to be too prescriptive (which is good to some extent), but also because they're unfamiliar (which is bad).
*   Perhaps UX should be part of the horizontal review process and standards should have a dedicated UX considerations section.
*   The accessibility groups have learned to do reviews early on and it would make sense for UX to start at that point in the process as well, especially given the earlier point about use cases and end user stories.
*   UX needs to be fungible for it to be accessible.
*   From a website perspective, the lack of browser unification around UX makes it hard to create great end user experiences.


### Useful attestations / promises / policies; Operationalising ‘Contextual Integrity'

**Reporter**: Serge Egelman

**Summary by**: Marian Harbach

Following on from the first day's discussion on contextual integrity as well as the importance of structured descriptions of data sharing (aka policy), this breakout explored how we could improve the situation on the Web. It came up fairly quickly that the existing but retired P3P standard addresses a very similar problem. The group was wondering if it might be time to bring this line of work back, especially as the regulatory interest has evolved over the last 20 years. Learning from past mistakes with P3P, we could require developers to support something similar in order to get access to capabilities.

Users also likely have different expectations today and app stores are already catering to that with privacy nutrition labels. Browsers could at first only require the information to show it to users and later start more strict enforcement. As developers already struggle to do the right thing, having good tooling is important too. While any display of additional, developer-controlled information can be abused (and already is, for example on iOS), it was argued that this may still be better than providing no information at all. However, it puts some pressure on browsers to make clear which information is provided by them vs. the website and its developer. One way around that is to let the developer make claims in the content area in a structured way, for example using the HTML permission element discussed in other sessions.

However, any claim can also create additional user confusion and may make abuse more believable than it already is today. The group agreed that getting such a user interface right is non-trivial. Yet, it might be less important what exactly the website claimed about itself, but more important that a claim was made to begin with, as that allows for legal action by third parties. This was found to be similar to how privacy policies aren't meant for consumers either, but force sites to state a policy that can be audited by interested parties. Having claims made by a website would also allow reporting abuse that could then be enforced by a safe-browsing-like mechanism, making this a content moderation problem to some extent.

The group then also discussed more technical enforcement mechanisms, like a Manufacturer Usage Description being used in the IoT realm. One challenge with data sharing is that once it hits the server, the browser can't know what happens to it. Thus, non-technical solutions are very important.

As a first step towards declarations and enforcement, it was brought up that the notification capability is unique: all interactions are fully under the user agent's control, such as the permission prompt and the notification rendering. The capability is purely about the content being displayed. If there was cross-browser agreement on policy and what abuse means, there would be a means to evaluate if abuse happens, and intervene when it does.


### Use case driven spec work / Updating specs

**Reporter**: Ian Clelland

We discussed whether spec designs should be driven by use cases, or whether it is better to allow interesting unforeseen use cases to arise naturally. On the one hand, the W3C used to design specs starting with a set of use cases, and the API design was tailored to serve those use cases, rather than trying to expose, for instance, details of underlying hardware. There was a sentiment that many modern specs start with the idea that an interesting piece of hardware is being shipped on devices, and just try to expose it directly to the web, leaving use cases to developers to figure out. The alternate opinion was that sometimes innovation comes out of having access to hardware. WebUSB and Web Bluetooth technologies, for instance, have made new applications possible that would not have been, if the spec designers had restricted the API to narrow use cases.

The questions we brought up were around how do we balance being use-case-driven vs. giving opportunities to the long tail of websites which would benefit from an open API, and how do we reconcile the immediate desire to expose today's hardware with the idea that the web platform should be relevant decades from now?

Secondly, we discussed spec maintenance, with the specific context of permissions and permissions policy specs (although other related specs, such Geolocation and Device Orientation were brought up to point out that they have no active owners).  It was suggested that perhaps W3C should have a group committed to maintaining specs, like WHATWG does for HTML and Fetch.

Specifically for Permissions Policy and Permissions, the following topics were discussed:

*   We should integrate Permissions Policy with the Permission Registry, and ensure that the registry can serve both Permissions and Permissions Policy specs.
*   The document.featurePolicy API is not supported cross-browser, is poorly named, and is mostly redundant with permissions.query, but has very high use on web sites. Chrome, WebKit and Mozilla representatives agreed to meet regularly to try to define and implement a path to actual deprecation of that API.
*   Finally, a discussion on whether there could be a strict mode for Permissions Policy, similar to the Strict CSP proposal, to make accidental delegation of permissions more difficult, and to protect against a specific scenario of iframe injection by malicious third parties.


## Participant Feedback

After the workshop, we sent a feedback survey to all participants. As only 7 participants responded (3 in-person participants, 4 remote), we will only report on a few high-level themes here.

5 of 7 respondents indicated that the event was very much worth their time, the remaining two indicated a moderate value (on a scale from "not at all" to "extremely worth my time"). When asked about which aspects of the event provided value to them, most aspects were rated as provided substantial or a lot of value where applicable (discussion on day 1, hallway chats, social dinner and ad-hoc social activities after the official program, being able to attend remotely, and diversity in participants backgrounds). The availability of the slack channel for discussions as well as the breakout sessions on day 2 elicited a more varied response. Several participants indicated that these two aspects of the workshop did not provide as much value to them while others found the opposite.

When asked about their preferred format and cadence for this event, 5 of 7 respondents indicated a preference for a yearly cadence and 6 of 7 preferred a two day event over longer or shorter durations.

We also asked respondents to share ideas for improvements. These included:

*   A more active role of the program committee, querying registered attendees for topics of interest instead of soliciting position papers. This should be used to shape the agenda beforehand and provide newcomers some anonymity to help them participate more actively.
*   Making objectives and intended outcomes clearer from the outset, so that attendees unfamiliar with W3C workshops know what to expect.
*   Introduce the role of the W3C and how it works at the beginning.
*   Find a way to reduce the reliance on technical jargon, such that participants with less technical expertise can follow more easily.
*   Making more time for introductions.
*   Focus more on fleshing out ideas.
*   Give participants a better chance to contribute more equally, as some discussions were dominated by several people.
*   Try to invite participants with an even broader range of backgrounds, including other domains and jurisdictions

To keep the momentum going, respondents suggested the following:

*   Holding the event more frequently (see below as well)
*   Create subgroups of people to keep discussion going
*   Propose that certain people join specific w3c working groups
*   Participants should write up proposals and share them in slack or file issues against relevant standards.


## Acknowledgements and appreciation

Big thanks to all participants who made the trip to Munich or took time to attend remotely. Many participants mentioned the varied backgrounds of all participants as a key benefit of the workshop.

Thank you to Serena Chen, Balazs Engedy, Marian Harbach and Google for hosting the workshop.
