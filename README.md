# F5-iRule-LTM-based-DoD-Banners

![License](https://img.shields.io/badge/license-MIT-green)
![TMOS Version](https://img.shields.io/badge/TMOS-15.0%2B-red)
![F5 iRules](https://img.shields.io/badge/F5-iRules%20(Tcl)-FF6600?logo=f5&logoColor=white)

An LTM-only solution for presenting a one-time DoD Banner. 
Two formats are presented:
- iRule only solution with embedded html, css, and javascript
- iRule and iFile solution with html, css, and javascript contained in an iFile

Note that this solution expects HTTPS; if you require these banners on an HTTP virtual server, remove the "Secure" flag from every cookie that the iRule sets.

The iRule also implements a bypass URI that allows specific requests to skip the banner; see the iRule source for the URI and its behavior.

## Background

The use of a DoD Warning Banner is a Defense Information Systems Agency (DISA) Security Technical Implementation Guide (STIG) requirement that is typically assigned as a Category III line item.

**STIG Requirement:**
> "The BIG-IP Core implementation must be configured to display the Standard Mandatory DoD-approved Notice and Consent Banner before granting access to virtual servers. (STIG ID: F5BI-LT-000023)"

## Prerequisites

- Familiarity with F5's GUI and basic administration of the F5 application delivery controller
- This process should be performed on an offline test virtual server and migrated to a production virtual server upon successful testing and acceptance of the banner operation

## Available Banner Types

This solution includes three color variants of the DoD Warning Banner:

### Green Banner
<img width="1660" height="1080" alt="GREEN_banner_1660x1080" src="https://github.com/user-attachments/assets/9159faa8-62bd-4c75-8432-8c0f5642bd28" />

### Red Banner
<img width="1660" height="1080" alt="RED_banner_1660x1080" src="https://github.com/user-attachments/assets/ed3a040f-7c79-48e1-9a2d-d5eab0efc720" />

### Yellow Banner
<img width="1660" height="1080" alt="YELLOW_banner_1660x1080" src="https://github.com/user-attachments/assets/fda054fa-332d-48b0-9edc-9a1e29b8a1fa" />

## Banner Features

All banner implementations include:
- Modern responsive design for various screen sizes
- Accessibility features (focus indicators, semantic markup)
- Modern CSS animations and transitions
- DoD-compliant consent language and formatting

## Testing and Validation

After implementation:
1. Verify the banner displays correctly on the test virtual server
2. Validate the banner text matches DoD requirements
3. Confirm the "I ACKNOWLEDGE AND CONSENT" button functions properly
4. Test that users can proceed through to the application after consent
5. Test that the bypass URI functions as expected
6. Only migrate to production after successful testing and acceptance

## License

MIT License - see [LICENSE](LICENSE) file for details.

## Disclaimer

- This solution is **NOT** officially endorsed, supported, or maintained by F5 Inc.
- F5 Inc. retains all rights to their trademarks, including but not limited to "F5", "BIG-IP", "LTM", "APM", and related marks
- This is an independent, community-developed solution that utilizes F5 products but is not affiliated with F5 Inc.
- For official F5 support and solutions, please contact F5 Inc. directly

**Technical Disclaimer**

- This software is provided "AS IS" without warranty of any kind
- The authors and contributors are not responsible for any damages or issues that may arise from its use
- Always test thoroughly in non-production environments before deployment
- Backup your F5 configuration before implementing any changes
- Review and understand all code before deploying to production systems

By using this software, you acknowledge that you have read and understood these disclaimers and agree to use this solution at your own risk.

