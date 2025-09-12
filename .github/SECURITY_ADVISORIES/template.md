# Security Advisory Template

**⚠️ SECURITY ADVISORY ⚠️**

## Advisory Information

- **Advisory ID**: FTHG-[YYYY]-[NN] (e.g., FTHG-2024-01)
- **Publication Date**: [Date]
- **Severity**: [Critical/High/Medium/Low]
- **CVSS Score**: [Score if available]
- **Affected Versions**: [Version range]
- **Fixed Versions**: [Version range]

## Summary

[Brief description of the vulnerability]

## Impact

[Detailed description of potential impact]

### Affected Components
- [ ] FTHG Token Contract
- [ ] StakeLocker Contract
- [ ] DistributionManager Contract
- [ ] OracleManager Contract
- [ ] KYCSoulbound Contract
- [ ] OffchainStakeOrchestrator
- [ ] Other: [Specify]

### Risk Assessment
- **Confidentiality**: [None/Low/Medium/High]
- **Integrity**: [None/Low/Medium/High]
- **Availability**: [None/Low/Medium/High]
- **Financial Impact**: [None/Low/Medium/High/Critical]

## Technical Details

### Vulnerability Description
[Detailed technical description of the vulnerability]

### Attack Vector
[How the vulnerability could be exploited]

### Proof of Concept
```solidity
// Example code demonstrating the vulnerability
// (Sanitized to prevent actual exploitation)
```

### Root Cause Analysis
[What caused this vulnerability to exist]

## Remediation

### Immediate Actions Required
1. [Action 1]
2. [Action 2]
3. [Action 3]

### Patches Applied
- **Contract Updates**: [List of contract changes]
- **Configuration Changes**: [List of config changes]
- **Deployment Changes**: [List of deployment changes]

### Verification Steps
1. [How to verify the fix is working]
2. [How to confirm you're not affected]

## Timeline

| Date | Event |
|------|-------|
| [Date] | Vulnerability discovered |
| [Date] | Initial assessment completed |
| [Date] | Fix developed and tested |
| [Date] | Security advisory published |
| [Date] | Patches deployed |
| [Date] | All-clear issued |

## Affected Parties

### Users
- **Impact**: [Description of user impact]
- **Action Required**: [What users need to do]

### Integrators
- **Impact**: [Description of integrator impact]
- **Action Required**: [What integrators need to do]

### Infrastructure
- **Impact**: [Description of infrastructure impact]
- **Action Required**: [What infrastructure changes are needed]

## Communication

### Public Disclosure
- **Initial Disclosure**: [Date and method]
- **Detailed Disclosure**: [Date and method]
- **Community Notification**: [How community was notified]

### Stakeholder Notification
- **Core Team**: [When and how notified]
- **Major Users**: [When and how notified]
- **Partners**: [When and how notified]
- **Regulators**: [When and how notified, if applicable]

## Prevention Measures

### Process Improvements
1. [Process change 1]
2. [Process change 2]
3. [Process change 3]

### Technical Improvements
1. [Technical improvement 1]
2. [Technical improvement 2]
3. [Technical improvement 3]

### Monitoring Enhancements
1. [Monitoring enhancement 1]
2. [Monitoring enhancement 2]
3. [Monitoring enhancement 3]

## Credits

### Discovery
- **Reported by**: [Name/Organization]
- **Discovery Date**: [Date]
- **Disclosure Method**: [How it was reported]

### Response Team
- **Security Lead**: [Name]
- **Development Lead**: [Name]
- **Communications Lead**: [Name]

### External Support
- **Security Auditors**: [If involved]
- **Legal Counsel**: [If involved]
- **Regulatory Bodies**: [If involved]

## References

### Internal Documentation
- [Link to internal post-mortem]
- [Link to technical analysis]
- [Link to fix documentation]

### External Resources
- [Link to CVE if applicable]
- [Link to security research]
- [Link to related advisories]

### Code Changes
- **Pull Request**: [Link to fix PR]
- **Commit Hash**: [Hash of fix commit]
- **Deployment Transaction**: [Transaction hash]

## Contact Information

### Security Team
- **Email**: security@fthboss.com
- **PGP Key**: [Key fingerprint]
- **Response Time**: 24-48 hours

### Emergency Contacts
- **Critical Issues**: [Emergency contact method]
- **After Hours**: [After hours contact method]
- **Media Inquiries**: [Media contact]

---

## Appendix

### Technical Artifacts
[Any technical logs, screenshots, or additional evidence]

### Legal Considerations
[Any legal implications or considerations]

### Regulatory Impact
[Any regulatory reporting or compliance implications]

---

**Classification**: [Public/Confidential/Restricted]  
**Distribution**: [Who should receive this advisory]  
**Review Date**: [When this advisory should be reviewed/updated]

---

*This security advisory follows the responsible disclosure principles and aims to provide clear, actionable information to help secure the FTH-G ecosystem.*