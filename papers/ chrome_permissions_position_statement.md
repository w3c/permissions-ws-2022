# Chrome Permissions Team — Position Statement

Authors:
 - engedy@chromium.org
 - sereeena@chromium.org
 - mharbach@google.com

## Our Background

The Chrome Permissions team believes that the web platform is most successful when it offers users meaningful controls for capabilities, and frames those controls in terms of questions users can meaningfully answer. Our mission is to enhance comprehension of controls for existing web platform capabilities, to reduce interruptions and dark patterns on the web at large — ultimately improving contextual integrity — and to build the next-generation framework that enables developers to rely on capable APIs to build delightful products, and enables users to use those products safely.

## Topics

### User agents should take more responsibility for the user journey leading up to a permission prompt

Controlling access to capabilities should happen at contextually relevant moments of the user’s journey. However, web browsers today have little to no insight into the user flow that takes place in the content area of the web application, and must rely entirely on the web application to follow best practices and to trigger the trusted permission UI only when it is expected by users.

To ensure both ease of use and user control, user agents should take more responsibility for shaping the steps of the user flow leading up to the point when the trusted permission UI is shown. One way of doing so could be for platforms to design prefabricated UI elements for developers to embed into their user flows. The design of these elements would capture what developers following best practices already show to users before triggering the platform-level prompt.

### User agents should frame controls in terms of questions users can meaningfully answer

Most web browsers currently rely on simple permission prompts that ask the user to make decisions about individual capabilities, with the capabilities themselves often being technical and low-level. As powerful APIs increase in both number and sophistication, it is getting increasingly harder for users to meaningfully reason about the set of capabilities truly needed for a certain function of a web application, and about the associated risks.

We envision combining a number of approaches to move beyond simple prompts as the primary means of capability control, and to experiment with novel approaches, including:
 - avoiding prompts altogether by integrating trustworthy controls into the user flow;
 - thematic grouping of permissions to form more easily understood clusters and reduce the number of necessary prompts;
 - prompting for purpose instead of capability access (“meet.example.com would like to have access to video conferencing functionality”); and
 - finding ways to assist users with reasoning about risks that are very far removed from primary tasks, such as fingerprinting and spoofing.

### User agents should provide usable & intuitive controls for ephemeral permission grants

Presently, most permission decisions in Chrome are persistent. Some browsers and mobile platforms already offer ephemeral permission grants, and we are hoping that the feature will become widely available across web browsers in the near future.

We are also seeing a number of challenges unique to the web platform that we need to solve to build controls that are both effortlessly usable in real-world use cases and intuitively understood by users. These challenges include complex navigation and usage patterns on the drive-by web, user expectations around the ephemeral nature of websites, and handling of multiple tabs or windows from the same security origin.
