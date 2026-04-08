# Final Design Report
A comprehensive report of the progress made and assignments completed for CS 5001 and CS 5002.

**Table of Contents**
1. [Project Abstract](#project-abstract) and [Project Description](#project-description)
2. [User Interface Specification](#user-interface-specification)
3. [Test Plan and Results](https://docs.google.com/document/d/1VAv-kXj0xt_tmkr2aNzBSpt-zs909jjMBfaCugWjLR0/edit?usp=sharing)
4. [User Manual](#user-manual)
5. [Spring Final PPT](https://docs.google.com/presentation/d/1alerdk5PkAvUmfofzCAMaawcI_n05nCEj53FGhospOw/edit?usp=sharing)
6. [Final Expo Poster](https://mailuc-my.sharepoint.com/:b:/g/personal/long2kw_mail_uc_edu/IQDpgASoLw6nTpQM67o1AOqIAZyrxnKD3RLASNFnpYQrFhU?e=urd9ug)
7. [Assessments](#self-assessment-essays)
8. [Summary of Hours and Justification](#summary-of-hours-and-justification)
9. [Summary of Expenses](#summary-of-expenses)
10. [Appendix](#appendix)

## Team Names
**Advisor**:
- Dr. Jillian Aurisano

**Team Members**:
- Anne Ning
- Jack Detrick
- Jonah Carter
- Kevin Long

## Abstract
A cross-platform mobile app that makes it dead-simple to share the correct contact info with the correct people. Allows for both granular control over the details shared with each person and pre-saved profiles to make any type of contact sharing a breeze! Utilizing technologies like NFC, RFID, and QR codes our focus is on making the experience frictionless for both the sharer and the receiver.

## Project Description
A cross-platform mobile app that makes it *dead-simple* to share the correct contact info with the correct people *every time*. Our app will allow granular control over the details shared with each person and come with pre-saved profiles to make business, personal, and any other category of contact information sharing a breeze!

Our focus is on making the experience as frictionless for both the sharer and the receiver as possible. We plan to utilize technologies like NFC, RFID, and QR codes to offer a sharing experience that works in all situations, regardless of internet connection, or the busyness of the environment with intelligent fallbacks depending on the surroundings.

## User Interface Specification
We spent a lot of time sketching and thinking about how to make our app as intuitive and user-friendly as possible.

That required a lot of design ideation and iteration. Below you can see a snapshot of some of our design ideas and iterations.

![A screenshot showing our sketches and prototypes in Figma](/images/ui-spec.png)

## User Manual
Our full user manual can be found [here](https://github.com/PlaceholderGroup/app/wiki).

Our FAQ has been copied over to this report and can be viewed below.

### What devices are supported?
Any and all recent smartphones are supported! We support both iOS (v15+) and Android (v7+).

### Is my data secure?
Yes. Your contacts are stored securely on your device. When you share your contact info it is sent directly from your device to the other person, we never see it or process it on any of our servers.

### Do I need an internet connection to share?
No. Our intuitive and direct sharing never requires an internet connection meaning you can easily share at anytime from anywhere!

### Does the other person need the app?
No. You can share your contact information with anyone, whether they have the app or not! Some rich features and sharing methods are only available if both users have the app, but basic contact sharing will always work with anyone who has a smartphone.

### Why is some information (photos, etc.) not showing up?
Depending on the method you use to share and the receiver's contact app not all features are supported. Images, for example, are too large for QR codes so any contacts shared with QR codes will not include images.

Your default iOS and Android contact apps support different features so not all information may display in each.

### Will shared contacts appear in my default apps (messages, contacts, etc.)?
Yes! While you can absolutely use our app to manage all your contacts we save them in a way to make them maximally compatible with all your default apps! Your contacts will appear in all the usual places like your messages, phone, email, and contacts apps.

## Self-Assessment Essays
- Anne Ning
  - [Initial](/individual/anne/assessment.md)
  - [Final]()
- Jack Detrick
  - [Initial](/individual/jack/Individual%20Capstone%20Assessment.pdf)
  - [Final]()
- Jonah Carter
  - [Initial]()
  - [Final]()
- Kevin Long
  - [Initial](/individual/kevin/assessment.md)
  - [Final](/individual/kevin/final-assessment.md)

## Summary of Hours and Justification
- Anne Ning
- Jack Detrick
- Jonah Carter
- Kevin Long
  - I did not track the exact number of hours I spent on this project. I am however confident that it is well over 45 hours even in just the past month, let alone the whole span of the project and semester. In addition to [the many commits](https://github.com/PlaceholderGroup/app/commits/main/) I made to the repository, I also frequently joined in and contributed to official and unofficial team meetings and discussions. I additionally performed extensive research into each of the components of our project, most notably the sharing technologies and data interchange formats we used.

## Summary of Expenses
As of 2026/04/08 we have not had any project related expenses.

## Appendix

### Code
We maintained our code in a separate repository.

> [PlaceholderGroup/app](https://github.com/PlaceholderGroup/app/)

We additionally created a fork of [`react-native-hce`](https://github.com/appidea/react-native-hce/) to add MIME type (and therefore vCard support).

> [PlaceholderGroup/react-native-hce](https://github.com/PlaceholderGroup/react-native-hce/tree/mime-type)

After cleaning these changes up we hope to contribute them to the upstream project.
