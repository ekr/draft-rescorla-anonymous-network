---
title: "Security Requirements for the IETF Network"
abbrev: "IETF Network Security"
category: bcp

updates: rfc8718
docname: draft-rescorla-anonymous-network-latest
submissiontype: IETF  # also: "independent", "editorial", "IAB", or "IRTF"
number:
date:
consensus: true
v: 3
status: bcp
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
    email: "ekr@rtfm.com"
 -
    fullname: "Richard Barnes"
    email: "rlb@ipv.sx"
 -
    fullname: "David Schinazi"
    email: "dschinazi.ietf@gmail.com"
 -
    fullname: "Tommy Pauly"
    email: "tpauly.ietf@gmail.com"

normative:

informative:

...

--- abstract

This document requires the network at the IETF plenary meeting
to protect the security and privacy of its users.


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

A critical, but implicit requirement in this paragraph is that IETF participants
need to be secure in their use of the Internet.  It will clearly have a material
impact on participants' Internet use if they cannot use the security
technologies they require, or if accessing the IETF network requires them to
reduce their security or privacy posture (e.g., by revealing sensitive information).

As expressed in {{?RFC7258}}, the IETF considers pervasive monitoring an attack,
The IETF has a long history of developing protocols to protect the
confidentiality and authenticity of Internet communications, such as IPsec,
DNSSEC, TLS, and SSH.  More recently, there has been a focus on protecting the
identities of the endpoints to communication, e.g., MASQUE, OHAI, and ECH.  The
security properties of the IETF network should be aligned with these principles.

For example:

* IETF attendees often employ mechanisms such as IPsec, HTTPS, Oblivious HTTP, and TLS ECH
  to protect the security and privacy of their business and day-to-day Internet
  usage. If these security features cannot be used, attendees will not be able
  to use the Internet as they need to.

* IETF attendees typically expect that the IETF network will not collect more
  information about their usage of it than is technically necessary to operate
  the network.  If IETF users need to authenticate in a way that their Internet
  traffic can be attributed to them by local or upstream network operators, this
  expectation would be violated, and attendees might not be willing or able to use the
  Internet under such circumstances.

This document updates the requirements of {{!RFC8718}} to make these security
requirements explicit.

## Conventions and Definitions

{::boilerplate bcp14-tagged}


# Requirements

This document extends the mandatory criteria as follows:

> The IETF network MUST be compatible with widely-used Internet security
> technologies, and MUST NOT interfere with their usage.  These properties MUST
> also hold for upstream networks.  In other words, in addition to global
> reachability at the IP layer, the network must provide secure global
> reachability, in the sense of being able to securely connect to any other
> endpoint on the Internet using any widely-used security protocol.

This text is intended to ensure that IETF participants can continue to get the
level of security that they require when they use the IETF network.

> The IETF network MUST NOT collect information about IETF participants'
> Internet usage beyond what is technically required to operate the network. If
> user-linked information needs to be collected, then it MUST NOT be
> disseminated beyond the immediate IETF network operational team, and MUST be
> deleted at the end of an IETF meeting.
>
> The IETF network MUST be accessible by any IETF participant without providing
> authentication information that is tied to their identity. If user-specific
> authentication is required, it MUST be possible for users to anonymously
> obtain an arbitrary number of credentials which are not linkable to their
> identity. The network SHOULD provide unauthenticated access or access via a
> shared credential if practicable.

This text is intended to maximize user privacy and forbid any
authentication mechanisms which would make it possible to
attribute traffic to a specific identifiable user.

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
