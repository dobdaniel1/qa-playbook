# EMV Level 3 Certification Readiness

Level 3 certification proves that a terminal or payment app, running a certified kernel, integrates correctly with the acquirer host for each card scheme. This checklist covers the work to do before booking a certification slot. Scheme-specific test plans come from the scheme or your accredited lab.

## Prerequisites

- [ ] EMV Level 1 (hardware) and Level 2 (kernel) approvals valid for the exact device and kernel versions
- [ ] Contactless kernel approvals for each scheme in scope
- [ ] Acquirer and scheme agreements in place, project registered with the scheme
- [ ] Certification test tool licensed and set up
- [ ] Test card set available for each scheme and entry mode
- [ ] Certification host environment available and stable

## Terminal configuration

- [ ] Terminal type, capabilities and additional capabilities set per the scheme profile
- [ ] AIDs, application version numbers and priority configured
- [ ] Terminal action codes (default, denial, online) loaded per scheme
- [ ] Floor limits, CVM limits and contactless transaction limits set
- [ ] CA public keys loaded for the test environment
- [ ] Merchant category code, country code and currency code correct
- [ ] Parameter file versioned and matches what will ship

## Host message checks

- [ ] Authorization request carries required ICC data (field 55)
- [ ] POS entry mode and condition code correct for every entry mode
- [ ] Reversal sent on timeout and on card decline after online approval
- [ ] Issuer script results returned in the next message where required
- [ ] Track 2 equivalent data and PAN sequence number sent correctly
- [ ] Amount, currency and STAN consistent across request, response and reversal

## Dry run

- [ ] Internal dry run of the full scheme test plan completed
- [ ] Logs captured for every case (terminal and host)
- [ ] Failures analysed and fixed before submission
- [ ] Receipts checked for required fields and masking

## Submission pack

- [ ] Implementation conformance statement completed
- [ ] Test logs and reports exported in the format the scheme expects
- [ ] Device, kernel and app versions recorded
- [ ] Contact list for scheme, lab, acquirer and vendor
