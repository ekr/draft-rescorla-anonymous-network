---
title: "Anonymous Access to the IETF Network"
abbrev: "Anonymous Access"
category: info

docname: draft-rescorla-anonymous-network-latest
submissiontype: IETF  # also: "independent", "editorial", "IAB", or "IRTF"
number:
date:
consensus: true
v: 3
# area: AREA
# workgroup: WG Working Group
keyword:
venue:
#  group: WG
#  type: Working Group
#  mail: WG@example.com
#  arch: https://example.com/WG
  github: "ekr/draft-rescorla-anonymous-network"
  latest: "https://ekr.github.io/draft-rescorla-anonymous-network/draft-rescorla-anonymous-network.html"

author:
 -
    fullname: "Eric Rescorla"
    organization: Independent
    email: "ekr@rtfm.com"

normative:

informative:

...

--- abstract

This document requires the network at the IETF plenary meeting
to provide anonymous access.


--- middle

# Introduction

IETF meeting participants depend heavily on Internet access
during the IETF plenary meeting. The venue selection process
defined in {{!RFC8718}} makes a functional network a mandatory
criterion:

>     It MUST be possible to provision Internet Access to the Facility
>     and IETF Hotels that allows those attending in person to utilize
>     the Internet for all their IETF, business, and day-to-day needs;
>     in addition, there must be sufficient bandwidth and access for
>     remote attendees.  Provisions include, but are not limited to,
>     native and unmodified IPv4 and IPv6 connectivity, and global
>     reachability; there may be no additional limitation that would
>     materially impact their Internet use.  To ensure availability, it
>     MUST be possible to provision redundant paths to the Internet.

This criterion does not require that access be anonymous; if IETF
users need to authenticate to use the network, thus potentially opens
up IETF participant's activity to surveillance.  The IETF has
determined {{?RFC7258}} that pervasive monitoring is an attack on the
Internet. This document requires that the IETF network provide
anonymous access, thus helping to mitigate this form of attack.


# Requirements

This document extends the mandatory criteria as follows:

>     The IETF network MUST be accessible by any IETF participant
>     without providing authentication information that is tied
>     to their identity. If user-specific authentication is
>     required, it MUST be possible for users to anonymously
>     obtain an arbitrary number of credentials which are not
>     linkable to their identity. The network SHOULD provide
>     anonymous access or access via a shared credential if
>     practicable.

[TODO: I would prefer to favor no authentication, but I think that
will just make it harder].

This text is intended to maximize user privacy and forbid any
authentication mechanisms which would make it possible to
attribute traffic to a specific identifiable user.


# Conventions and Definitions

{::boilerplate bcp14-tagged}


# Security Considerations

The requirement in this document enhances user security and privacy by
reducing a network observer's ability to track user behavior.
The requirement may make it more difficult to manage abusive behavior
by network users, however, the IETF network currently routinely operates in
a mode without any user-level authentication, so this requirement
does not create a security regression.


# IANA Considerations

This document has no IANA actions.


--- back

# Acknowledgments
{:numbered="false"}

TODO acknowledge.
