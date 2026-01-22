# PROMO lineup limitations overview

The PROMO lineup is designed as a budget-friendly option for non-critical workloads, testing environments, educational use, and personal projects.  
To keep pricing at this level, several limitations apply.

---

## Service and support limitations
- No support SLA or uptime guarantee.
- Technical support is not included; only basic guidance is provided if possible.
- We will not ignore your requests, but response times will be significantly longer compared to standard plans.
- Complex tasks (such as software installation, debugging, or configuration) will **not** be fulfilled by support.
- Referral program payouts and discounts do not apply to the lineup.

## Operating system and installation limitations
- Windows OS is not supported.
- Custom ISO mounting is unavailable.
- Only official OS templates may be used.

## Performance limitations
- Shared NVMe storage is used, with various IOPS caps depending on the plan used:  
 DE-PROMO-1 - **8k IOPS** per VPS  
 DE-PROMO-2 - **16k IOPS** per VPS  
 DE-PROMO-3 - **24k IOPS** per VPS  
 DE-PROMO-4 - **32k IOPS** per VPS  
- Fair-share CPU model with guaranteed usage of **up to 25%** of the assigned vCPU.
- Sustained 100% network load may trigger traffic shaping under the **[Fair Use Policy](https://senko.digital/acceptable-use-policy)**.

## Network limitations
- Network throughput is limited per plan specification.
- Outgoing mail ports (SMTP, 25/465/587) cannot be opened under any circumstances.
- Continuous uplink saturation is prohibited.

## Recommended use cases
These plans are suitable for:
- development and testing environments  
- staging setups  
- experimental or temporary projects  
- personal VPN  
- personal website or simple web hosting  
- learning, practicing, and exploring Linux  

They are **not recommended** for anyone requiring high availability and guaranteed server performance.
