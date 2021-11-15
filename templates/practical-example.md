<!--
Use this template when your project is fairly complex and difficult and you want to focus on choosing an option.
Source: https://medium.com/swlh/a-practical-guide-to-writing-a-software-technical-design-document-c6f4d865ccff
-->

# Speech-to-Text App TDD

## Problem

<!-- Provide a concise description of an issue to be addressed, or a process to be improved upon. -->

We would like to design a Speech-to-Text app for Android devices. A user can tap on a button on the app, and the transcript will show up on the screen as the user speaks.

## Background

<!-- This section paints the context to the reviewers, and clarifies why we need to solve this problem. -->

According to recent research and interviews with Patent Attorneys, we noticed there is an increasing need to auto dictate while interviewing their clients. Patent Attorneys also needs to review the original voice recordings if the transcript is not accurate.

## Goals

<!-- Describe everything you want to achieve with this design. -->

1. The transcribing accuracy rate can have 90% and higher.
2. The speech binary data can be captured and stored for future auditing.
3. Keep the size of the Android APK under 100 MB.
4. The transcribing process should be continuous, meaning that the user can see the transcripts while the user is talking.

## Non-Goals

<!-- Draw boundaries outside which will not be considered. Explain why. -->

1. Build the speech data auditing process. Reason: we will decide on how to build this later. Currently, we need to preserve user info and speech data.

## Design Options

<!-- Pick the most reasonable 3 or 4 options to consider. For each option, describe in detail what the proposed system looks like.  For each option, provide an exhaustive list of pros and cons.  -->

### Option 1: The app calls a cloud-based Automatic Speech Recognition (ASR) service directly

We could use a 3rd party cloud service (such as Amazon Autotranscribe, Google Speech-to-Text) directly. The Android app can make requests to the ASR service directly, and display the response to the screen immediately.

Pros:

1. By now, a mature ASR service such as Amazon Transcribe is able to provide 95% and over transcribing accuracy. (This meets Goal #1)
2. No need to set up a server.

Cons:

1. The speech binary data cannot be captured. (This is against Goal #2)
2. The 3rd party ASR service is not free.

### Option 2: Build the pre-trained embedded ASR in the App

Pros:

Cons:

### Option 3: A HTTP/1.1 service makes proxy calls to a cloud-based Automatic Speech Recognition (ASR) service

We could set up a proxy service between the Android app and a 3rd party cloud service (such as Amazon Autotranscribe, Google Speech-to-Text). When the user taps the button, the speech binary data is recorded on the app and sends it to the proxy service. As the proxy service pipes the data to the ASR service, it can also grab the data and store it elsewhere (For example, Google Storage).

Pros:

1. Google Speech-to-Text service can provide 95% transcribing accuracy. (This meets Goal #1)
2. The speech binary data can be captured and stored. (This meets Goal #2)
3. The Android app would be a thin client without doing transcribing itself. The size of the app cannot increase significantly. (This meets Goal #3)

Cons:

1. An additional service needs to be set up. However, it is very easy to set up a service with HTTP/1.1.
2. The transcribing process would not be continuous because of the one-directional nature of the HTTP/1.1 service. (This is against Goal #4)

### Option 4: A bidirectional RPC service to proxy calls to a cloud-based ASR service

![Option 4](https://miro.medium.com/max/1344/1*07iudFxdWXm_gDGNuwv9kw.jpeg)

**Pros**

Cons:

#### Conclusion

<!-- Based on all the analysis in-depth, you will start to see the best option start to emerge by having more pros or all pros that meet the Goals. The chosen solution can also have cons, which are often not deal breakers for the decision. In this section, we can also add what we will do to mitigate the cons of the chosen option. -->

Based on the analysis above, the proposed approach is Option 4, which meets all the Goals.
