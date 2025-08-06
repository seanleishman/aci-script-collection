# Cisco ACI Automation Scripts

This repository contains a collection of Python scripts developed to automate and interact with Cisco Application Centric Infrastructure (ACI) environments. These scripts were originally developed for internal use during my time at Cisco to assist customers with operational tasks, visibility, and data extraction.

They are shared here for educational and demonstration purposes to showcase my experience working with Cisco ACI, REST APIs, and network automation. These are *not* official Cisco tools. Feel free to check them out and of course let me know if there are any questions or comments you may have.

Please note that there is **no APIC / ACI Fabric** tied to these scripts, it is up to the user to setup their own testing APIC & fabric to run these against. There are no hard coded credentials, users are prompted for APIC username, password, and IP when running each script.

---

## Features

- APIC Authentication and Token Management
- vPC/Port Channel VLAN Associtaion Report
- vPC CDP & LLDP Neighbor Relationships Report
- Conditional Interface Policy Group LLDP Disablement
- ACI Fabric Switch Bootflash Report

---

## Structure

Each script is standalone and documented with comments explaining functionality and usage.

The repository is organized into the following tree sctructure:

aci-python-tools/
├── README.md
├── LICENSE
├── requirements.txt
├── scripts/
│   ├── get_lldp_neighbors.py
│   ├── bootflash_checker.py
│   ├── vpc_report_generator.py
│   └── ...
├── utils/
│   ├── apic_login.py
│   └── common_functions.py
└── examples/
    └── sample_output.txt

## Pre-Requisites

- You should already have an enviroment with the latest versions of **git**, **pip**, and **python** already set up

- These scripts are up do date and tested with the latest versions of Python, namely **Python 3.13.5**

- To install all neccesary dependencies, I recommend to create a python virtual environment for isolation of your local environment.

## Running

After cloning the repository, run the following in the root directory to install all neccesary dependancies:

`pip install -r requirements.txt`

Check the **/examples** folder for information about each script that will contain:

1. Explanation of the script and what it is accomplishing
2. Script flow and how it works
3. Expected results
4. Details in executing how to run (some scripts vary in needing specefic inputs or flags)
