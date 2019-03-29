---
title: Hardcoded Roles in PeopleCode/SQL
layout: en
permalink: /posts/peopletools/hardcoded_roles/
---

Ever spent a few hours wondering (and then tracing) just to see why you couldn't get see data on a particular page?  

Let this list help you...

Tip: To add a role to this list, clone one of the existing.

# PeopleTools

## PeopleSoft Administrator

*Role name* PeopleSoft Administrator

*Navigation* All components

*Purpose* Bypasses permission list security on all components

*Offending Object* Internal C++ appserver logic

## Portal Administrator

*Role name* Portal Administrator

*Navigation* All portal objects

*Purpose* Bypasses permission list security on all portal objects

*Offending Object* Internal C++ appserver logic

## Pivot Grid Administrator

*Role name* PivotGridAdmin

*Navigation* Reporting Tools > Pivot Grid > Pivot Grid Wizard

*Purpose* Allows role member to see all pivot grids (including delivered from the PI), not just the ones you created

*Offending Object* Record PSPGCORE_DVW

Todo: add in more detail:

- ProcessSchedulerAdmin
- ADS Designer
- ReportDistAdmin
- Search Administrator
- Search Developer
- XMLP Report Developer

# HCM

# Financials

# Campus

# Cloud
