# Security Policy

  ## Supported Versions

  This repository provides the Bisq-maintained fork of `jtorctl`, a Java Tor
  control-port library supplemented with patches from the Briar project. It is
  used to communicate with Tor's control interface.

  Security fixes are applied to the active Bisq-maintained branch and any active
  maintenance branch still used by supported Bisq applications.

  | Version / Branch | Supported |
  | --- | --- |
  | `master` | :white_check_mark: |
  | Active maintenance branches used by supported Bisq applications | :white_check_mark: |
  | Legacy branches, unsupported forks, or locally modified builds | :x: |

  Vulnerabilities in Tor itself should also be reported to the Tor Project
  according to its own security policy. Vulnerabilities in upstream `jtorctl` or
  Briar-derived patches should be coordinated with the relevant upstream project
  when appropriate. This policy covers the Bisq-maintained fork and its integration
  risk for Bisq applications.

  ## Reporting a Vulnerability

  Please do **not** report security vulnerabilities through public pull requests,
  Matrix rooms, forums, or social media.

  Report suspected vulnerabilities privately through GitHub's **Report a
  vulnerability** flow on this repository's Security page. If that option is not
  available, contact Bisq maintainers through the main Bisq project security
  channel and ask for a private reporting path. Do not include exploit details in
  public channels.

  Include as much detail as possible:

  - affected branch, commit, dependency, or consuming Bisq application;
  - affected component, such as `TorControlConnection`, authentication,
    command formatting, reply parsing, event handling, password digest handling,
    timeout handling, or examples;
  - whether the issue affects Tor control-port authentication, control command
    injection, hidden service management, event spoofing, control credential
    exposure, unsafe logging, or denial of service;
  - whether the issue can expose user IP addresses, onion service identity,
    control-port credentials, private network metadata, or application behavior;
  - reproduction steps, logs, Tor control protocol transcripts, malformed replies,
    or proof of concept code where useful;
  - whether the issue depends on a malicious local process, compromised Tor
    process, untrusted control-port endpoint, malformed control response, or
    unexpected network/proxy configuration.

  Bisq is an open-source project maintained by contributors. Response times may
  vary, but reports involving Tor control authentication bypass, command injection,
  credential exposure, onion service compromise, IP leakage, or traffic
  deanonymization are treated as urgent security issues and will be triaged as
  quickly as possible.

  For lower-severity issues, maintainers will respond when contributor capacity is
  available.

  If the report is accepted, maintainers may coordinate a fix privately, prepare a
  patched branch or dependency update, notify Tor/Briar/upstream maintainers when
  appropriate, and publish an advisory after users have had a reasonable
  opportunity to update. If the report is declined, maintainers will explain the
  reason when possible.

  Please give maintainers reasonable time to investigate and release mitigations
  before public disclosure. For severe or actively exploited issues, coordinate
  timing with maintainers so public details do not increase risk to users.

  Bisq does not currently guarantee a bug bounty. Security work may be eligible
  for Bisq DAO compensation if it qualifies under the project's contributor and
  critical-bug processes.
