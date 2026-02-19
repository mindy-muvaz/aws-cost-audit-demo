© 2025 MuVaz Consulting, LLC - Sample Report for Demonstration
   Get the tool: awsaudit.muvazconsulting.com




# AWS Cost Optimization Audit Report

**Generated:** 2026-02-18 16:31:57 UTC

**Tool Version:** 2.0.0

## Executive Summary

- **Total Findings:** 28
- **Estimated Monthly Savings:** $106.70
- **Regions Scanned:** 2
- **Services Analyzed:** CloudWatch Logs, EBS, EC2

### Findings by Severity

- **High:** 10
- **Medium:** 18

### Top Savings Opportunities

1. **EBS** - vol-0008363d5107c5604: $15.00/month
   - Unattached gp2 volume (150 GB)

2. **EBS** - vol-0beb612f2902fad91: $15.00/month
   - Unattached gp2 volume (150 GB)

3. **EBS** - vol-0045f213635ec31da: $10.00/month
   - Unattached gp2 volume (100 GB)

4. **EBS** - vol-0d6eeca25d24e12fb: $10.00/month
   - Unattached gp2 volume (100 GB)

5. **EBS** - vol-01d6b0f4ad3308f08: $6.40/month
   - Unattached gp3 volume (80 GB)

6. **EBS** - vol-06f05d4f1c8555514: $6.40/month
   - Unattached gp3 volume (80 GB)

7. **EBS** - vol-0e09a6308fbcff154: $4.00/month
   - Unattached gp3 volume (50 GB)

8. **EBS** - vol-00d675a904f9984e2: $4.00/month
   - Unattached gp3 volume (50 GB)

9. **EC2** - eipalloc-0421046bfc5f1b6ae: $3.65/month
   - Unassociated Elastic IP incurring hourly charges

10. **EC2** - eipalloc-041400c8c6823f70e: $3.65/month
   - Unassociated Elastic IP incurring hourly charges

## Detailed Findings

### Region: us-east-1

**Regional Savings Potential:** $53.35/month

#### CloudWatch Logs

**[Medium]** `/aws/apigateway/demo-api-demo-20260218-092800`
- **Issue:** No retention policy (logs stored indefinitely)
- **Recommendation:** Set retention to 30 days or use S3 archival
- **Details:** {"stored_bytes": 0}

**[Medium]** `/aws/demo/audit-test-demo-20260218-092800`
- **Issue:** No retention policy (logs stored indefinitely)
- **Recommendation:** Set retention to 30 days or use S3 archival
- **Details:** {"stored_bytes": 0}

**[Medium]** `/aws/lambda/old-function-demo-20260218-092800`
- **Issue:** No retention policy (logs stored indefinitely)
- **Recommendation:** Set retention to 30 days or use S3 archival
- **Details:** {"stored_bytes": 0}

**[Medium]** `/ecs/demo-service-demo-20260218-092800`
- **Issue:** No retention policy (logs stored indefinitely)
- **Recommendation:** Set retention to 30 days or use S3 archival
- **Details:** {"stored_bytes": 0}

#### EBS — $42.40/month

**[High]** `vol-0008363d5107c5604`
- **Issue:** Unattached gp2 volume (150 GB)
- **Recommendation:** Delete volume if no longer needed, or create snapshot and delete
- **Potential Savings:** $15.00/month
- **Details:** {"size_gb": 150, "type": "gp2", "state": "available"}

**[High]** `vol-0045f213635ec31da`
- **Issue:** Unattached gp2 volume (100 GB)
- **Recommendation:** Delete volume if no longer needed, or create snapshot and delete
- **Potential Savings:** $10.00/month
- **Details:** {"size_gb": 100, "type": "gp2", "state": "available"}

**[High]** `vol-01d6b0f4ad3308f08`
- **Issue:** Unattached gp3 volume (80 GB)
- **Recommendation:** Delete volume if no longer needed, or create snapshot and delete
- **Potential Savings:** $6.40/month
- **Details:** {"size_gb": 80, "type": "gp3", "state": "available"}

**[High]** `vol-0e09a6308fbcff154`
- **Issue:** Unattached gp3 volume (50 GB)
- **Recommendation:** Delete volume if no longer needed, or create snapshot and delete
- **Potential Savings:** $4.00/month
- **Details:** {"size_gb": 50, "type": "gp3", "state": "available"}

**[High]** `vol-06bb1e89419f66f8b`
- **Issue:** Unattached gp2 volume (20 GB)
- **Recommendation:** Delete volume if no longer needed, or create snapshot and delete
- **Potential Savings:** $2.00/month
- **Details:** {"size_gb": 20, "type": "gp2", "state": "available"}

**[Medium]** `vol-0008363d5107c5604`
- **Issue:** gp2 volume can be migrated to gp3 (150 GB)
- **Recommendation:** Modify volume type to gp3 for better price/performance
- **Potential Savings:** $3.00/month
- **Details:** {"size_gb": 150, "current_type": "gp2"}

**[Medium]** `vol-0045f213635ec31da`
- **Issue:** gp2 volume can be migrated to gp3 (100 GB)
- **Recommendation:** Modify volume type to gp3 for better price/performance
- **Potential Savings:** $2.00/month
- **Details:** {"size_gb": 100, "current_type": "gp2"}

#### EC2 — $10.95/month

**[Medium]** `eipalloc-0421046bfc5f1b6ae`
- **Issue:** Unassociated Elastic IP incurring hourly charges
- **Recommendation:** Release EIP if not needed, or associate with an instance
- **Potential Savings:** $3.65/month
- **Details:** {"public_ip": "100.51.103.143"}

**[Medium]** `eipalloc-041400c8c6823f70e`
- **Issue:** Unassociated Elastic IP incurring hourly charges
- **Recommendation:** Release EIP if not needed, or associate with an instance
- **Potential Savings:** $3.65/month
- **Details:** {"public_ip": "34.235.239.63"}

**[Medium]** `eipalloc-06f949382c5c8c2d3`
- **Issue:** Unassociated Elastic IP incurring hourly charges
- **Recommendation:** Release EIP if not needed, or associate with an instance
- **Potential Savings:** $3.65/month
- **Details:** {"public_ip": "54.242.101.106"}


### Region: us-east-2

**Regional Savings Potential:** $53.35/month

#### CloudWatch Logs

**[Medium]** `/aws/apigateway/demo-api-demo-20260218-092844`
- **Issue:** No retention policy (logs stored indefinitely)
- **Recommendation:** Set retention to 30 days or use S3 archival
- **Details:** {"stored_bytes": 0}

**[Medium]** `/aws/demo/audit-test-demo-20260218-092844`
- **Issue:** No retention policy (logs stored indefinitely)
- **Recommendation:** Set retention to 30 days or use S3 archival
- **Details:** {"stored_bytes": 0}

**[Medium]** `/aws/lambda/old-function-demo-20260218-092844`
- **Issue:** No retention policy (logs stored indefinitely)
- **Recommendation:** Set retention to 30 days or use S3 archival
- **Details:** {"stored_bytes": 0}

**[Medium]** `/ecs/demo-service-demo-20260218-092844`
- **Issue:** No retention policy (logs stored indefinitely)
- **Recommendation:** Set retention to 30 days or use S3 archival
- **Details:** {"stored_bytes": 0}

#### EBS — $42.40/month

**[High]** `vol-0beb612f2902fad91`
- **Issue:** Unattached gp2 volume (150 GB)
- **Recommendation:** Delete volume if no longer needed, or create snapshot and delete
- **Potential Savings:** $15.00/month
- **Details:** {"size_gb": 150, "type": "gp2", "state": "available"}

**[High]** `vol-0d6eeca25d24e12fb`
- **Issue:** Unattached gp2 volume (100 GB)
- **Recommendation:** Delete volume if no longer needed, or create snapshot and delete
- **Potential Savings:** $10.00/month
- **Details:** {"size_gb": 100, "type": "gp2", "state": "available"}

**[High]** `vol-06f05d4f1c8555514`
- **Issue:** Unattached gp3 volume (80 GB)
- **Recommendation:** Delete volume if no longer needed, or create snapshot and delete
- **Potential Savings:** $6.40/month
- **Details:** {"size_gb": 80, "type": "gp3", "state": "available"}

**[High]** `vol-00d675a904f9984e2`
- **Issue:** Unattached gp3 volume (50 GB)
- **Recommendation:** Delete volume if no longer needed, or create snapshot and delete
- **Potential Savings:** $4.00/month
- **Details:** {"size_gb": 50, "type": "gp3", "state": "available"}

**[High]** `vol-062efb327212f1eec`
- **Issue:** Unattached gp2 volume (20 GB)
- **Recommendation:** Delete volume if no longer needed, or create snapshot and delete
- **Potential Savings:** $2.00/month
- **Details:** {"size_gb": 20, "type": "gp2", "state": "available"}

**[Medium]** `vol-0beb612f2902fad91`
- **Issue:** gp2 volume can be migrated to gp3 (150 GB)
- **Recommendation:** Modify volume type to gp3 for better price/performance
- **Potential Savings:** $3.00/month
- **Details:** {"size_gb": 150, "current_type": "gp2"}

**[Medium]** `vol-0d6eeca25d24e12fb`
- **Issue:** gp2 volume can be migrated to gp3 (100 GB)
- **Recommendation:** Modify volume type to gp3 for better price/performance
- **Potential Savings:** $2.00/month
- **Details:** {"size_gb": 100, "current_type": "gp2"}

#### EC2 — $10.95/month

**[Medium]** `eipalloc-0071f834889dc24e3`
- **Issue:** Unassociated Elastic IP incurring hourly charges
- **Recommendation:** Release EIP if not needed, or associate with an instance
- **Potential Savings:** $3.65/month
- **Details:** {"public_ip": "3.14.171.78"}

**[Medium]** `eipalloc-091679f0d3520c3c6`
- **Issue:** Unassociated Elastic IP incurring hourly charges
- **Recommendation:** Release EIP if not needed, or associate with an instance
- **Potential Savings:** $3.65/month
- **Details:** {"public_ip": "3.141.95.63"}

**[Medium]** `eipalloc-02225da745fa7fb81`
- **Issue:** Unassociated Elastic IP incurring hourly charges
- **Recommendation:** Release EIP if not needed, or associate with an instance
- **Potential Savings:** $3.65/month
- **Details:** {"public_ip": "3.22.178.56"}


## Appendix

### Methodology

This audit analyzes AWS resources across all enabled regions using read-only API calls. Cost estimates are based on standard on-demand pricing and may vary based on your specific AWS agreements, Reserved Instances, or Savings Plans.

### Recommendations

1. Review findings by severity, prioritizing Critical and High items
2. Validate recommendations in a non-production environment first
3. Consider Reserved Instances or Savings Plans for stable workloads
4. Implement AWS Cost Explorer and Budgets for ongoing monitoring
5. Schedule regular cost audits (monthly or quarterly)

