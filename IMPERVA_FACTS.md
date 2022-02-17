--I ran ansible fact gathering against my MX running on VMware.  This is just here for dev reference. 

ansible -i inventories/default/hosts 192.168.2.5 -u ansible --extra-vars "ansible_sudo_pass=your_password ansible_password=your_password ansible_become_method=su ansible_become_pass=your_password" -m setup
192.168.2.5 | SUCCESS => {
    "ansible_facts": {
        "ansible_all_ipv4_addresses": [
            "192.168.2.5"
        ],
        "ansible_all_ipv6_addresses": [
            "fe80::20c:29ff:fe77:203d"
        ],
        "ansible_apparmor": {
            "status": "disabled"
        },
        "ansible_architecture": "x86_64",
        "ansible_bios_date": "09/21/2015",
        "ansible_bios_version": "6.00",
        "ansible_cmdline": {
            "KEYBOARDTYPE": "pc",
            "KEYTABLE": "us",
            "LANG": "en_US.UTF-8",
            "SYSFONT": "latarcyrheb-sun16",
            "crashkernel": "129M@0M",
            "divider": "10",
            "notsc": true,
            "panic": "10",
            "quiet": true,
            "rd_LVM_LV": "sysvg/root.vol",
            "rd_NO_DM": true,
            "rd_NO_LUKS": true,
            "rd_NO_MD": true,
            "rhgb": true,
            "ro": true,
            "root": "/dev/mapper/sysvg-root.vol",
            "transparent_hugepage": "never"
        },
        "ansible_date_time": {
            "date": "2020-06-03",
            "day": "03",
            "epoch": "1591157992",
            "hour": "00",
            "iso8601": "2020-06-03T04:19:52Z",
            "iso8601_basic": "20200603T001952850583",
            "iso8601_basic_short": "20200603T001952",
            "iso8601_micro": "2020-06-03T04:19:52.850769Z",
            "minute": "19",
            "month": "06",
            "second": "52",
            "time": "00:19:52",
            "tz": "EDT",
            "tz_offset": "-0400",
            "weekday": "Wednesday",
            "weekday_number": "3",
            "weeknumber": "22",
            "year": "2020"
        },
        "ansible_default_ipv4": {
            "address": "192.168.2.5",
            "alias": "eth0",
            "broadcast": "192.168.2.255",
            "gateway": "192.168.2.2",
            "interface": "eth0",
            "macaddress": "00:0c:29:77:20:3d",
            "mtu": 1500,
            "netmask": "255.255.255.0",
            "network": "192.168.2.0",
            "type": "ether"
        },
        "ansible_default_ipv6": {},
        "ansible_device_links": {
            "ids": {
                "dm-0": [
                    "dm-name-sysvg-root.vol",
                    "dm-uuid-LVM-a7xGgPqn7lIJ5jY2CcGobwBsAFGyqVrF3zCB0NBsDFGfzCeUCMZmj0KdGqysfsdK"
                ],
                "dm-1": [
                    "dm-name-sysvg-swap.vol",
                    "dm-uuid-LVM-a7xGgPqn7lIJ5jY2CcGobwBsAFGyqVrFl4KeohZcGmzG98vg0DmvgXfVP2B4icNR"
                ],
                "dm-2": [
                    "dm-name-sysvg-var.vol",
                    "dm-uuid-LVM-a7xGgPqn7lIJ5jY2CcGobwBsAFGyqVrFUkuWKoIfbcVF8yPgmi75WyYUe2PBuAVd"
                ],
                "sda": [
                    "ata-VMware_Virtual_IDE_Hard_Drive_00000000000000000001",
                    "scsi-SATA_VMware_Virtual_00000000000000000001"
                ],
                "sda1": [
                    "ata-VMware_Virtual_IDE_Hard_Drive_00000000000000000001-part1",
                    "scsi-SATA_VMware_Virtual_00000000000000000001-part1"
                ],
                "sda2": [
                    "ata-VMware_Virtual_IDE_Hard_Drive_00000000000000000001-part2",
                    "scsi-SATA_VMware_Virtual_00000000000000000001-part2"
                ]
            },
            "labels": {},
            "masters": {
                "sda2": [
                    "dm-0",
                    "dm-1",
                    "dm-2"
                ]
            },
            "uuids": {
                "dm-0": [
                    "9e7897a8-f649-4c97-8438-161256cd3865"
                ],
                "dm-1": [
                    "9c7eed6d-ae2b-48e5-bd50-04db256c4144"
                ],
                "dm-2": [
                    "9756557e-7b49-44ef-8792-ecec9f95e37a"
                ],
                "sda1": [
                    "44e369cb-9174-46a4-80c7-4f15fa9bc4ad"
                ]
            }
        },
        "ansible_devices": {
            "dm-0": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [
                        "dm-name-sysvg-root.vol",
                        "dm-uuid-LVM-a7xGgPqn7lIJ5jY2CcGobwBsAFGyqVrF3zCB0NBsDFGfzCeUCMZmj0KdGqysfsdK"
                    ],
                    "labels": [],
                    "masters": [],
                    "uuids": [
                        "9e7897a8-f649-4c97-8438-161256cd3865"
                    ]
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "58720256",
                "sectorsize": "512",
                "size": "28.00 GB",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "dm-1": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [
                        "dm-name-sysvg-swap.vol",
                        "dm-uuid-LVM-a7xGgPqn7lIJ5jY2CcGobwBsAFGyqVrFl4KeohZcGmzG98vg0DmvgXfVP2B4icNR"
                    ],
                    "labels": [],
                    "masters": [],
                    "uuids": [
                        "9c7eed6d-ae2b-48e5-bd50-04db256c4144"
                    ]
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "6291456",
                "sectorsize": "512",
                "size": "3.00 GB",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "dm-2": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [
                        "dm-name-sysvg-var.vol",
                        "dm-uuid-LVM-a7xGgPqn7lIJ5jY2CcGobwBsAFGyqVrFUkuWKoIfbcVF8yPgmi75WyYUe2PBuAVd"
                    ],
                    "labels": [],
                    "masters": [],
                    "uuids": [
                        "9756557e-7b49-44ef-8792-ecec9f95e37a"
                    ]
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "270008320",
                "sectorsize": "512",
                "size": "128.75 GB",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "loop0": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "0",
                "sectorsize": "512",
                "size": "0.00 Bytes",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "loop1": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "0",
                "sectorsize": "512",
                "size": "0.00 Bytes",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "loop2": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "0",
                "sectorsize": "512",
                "size": "0.00 Bytes",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "loop3": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "0",
                "sectorsize": "512",
                "size": "0.00 Bytes",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "loop4": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "0",
                "sectorsize": "512",
                "size": "0.00 Bytes",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "loop5": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "0",
                "sectorsize": "512",
                "size": "0.00 Bytes",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "loop6": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "0",
                "sectorsize": "512",
                "size": "0.00 Bytes",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "loop7": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "0",
                "sectorsize": "512",
                "size": "0.00 Bytes",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "ram0": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "32768",
                "sectorsize": "512",
                "size": "16.00 MB",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "ram1": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "32768",
                "sectorsize": "512",
                "size": "16.00 MB",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "ram10": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "32768",
                "sectorsize": "512",
                "size": "16.00 MB",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "ram11": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "32768",
                "sectorsize": "512",
                "size": "16.00 MB",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "ram12": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "32768",
                "sectorsize": "512",
                "size": "16.00 MB",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "ram13": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "32768",
                "sectorsize": "512",
                "size": "16.00 MB",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "ram14": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "32768",
                "sectorsize": "512",
                "size": "16.00 MB",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "ram15": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "32768",
                "sectorsize": "512",
                "size": "16.00 MB",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "ram2": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "32768",
                "sectorsize": "512",
                "size": "16.00 MB",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "ram3": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "32768",
                "sectorsize": "512",
                "size": "16.00 MB",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "ram4": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "32768",
                "sectorsize": "512",
                "size": "16.00 MB",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "ram5": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "32768",
                "sectorsize": "512",
                "size": "16.00 MB",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "ram6": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "32768",
                "sectorsize": "512",
                "size": "16.00 MB",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "ram7": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "32768",
                "sectorsize": "512",
                "size": "16.00 MB",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "ram8": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "32768",
                "sectorsize": "512",
                "size": "16.00 MB",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "ram9": {
                "holders": [],
                "host": "",
                "links": {
                    "ids": [],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": null,
                "partitions": {},
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "",
                "sectors": "32768",
                "sectorsize": "512",
                "size": "16.00 MB",
                "support_discard": "0",
                "vendor": null,
                "virtual": 1
            },
            "sda": {
                "holders": [],
                "host": "IDE interface: Intel Corporation 82371AB/EB/MB PIIX4 IDE (rev 01)",
                "links": {
                    "ids": [
                        "ata-VMware_Virtual_IDE_Hard_Drive_00000000000000000001",
                        "scsi-SATA_VMware_Virtual_00000000000000000001"
                    ],
                    "labels": [],
                    "masters": [],
                    "uuids": []
                },
                "model": "VMware Virtual I",
                "partitions": {
                    "sda1": {
                        "holders": [],
                        "links": {
                            "ids": [
                                "ata-VMware_Virtual_IDE_Hard_Drive_00000000000000000001-part1",
                                "scsi-SATA_VMware_Virtual_00000000000000000001-part1"
                            ],
                            "labels": [],
                            "masters": [],
                            "uuids": [
                                "44e369cb-9174-46a4-80c7-4f15fa9bc4ad"
                            ]
                        },
                        "sectors": "512000",
                        "sectorsize": 512,
                        "size": "250.00 MB",
                        "start": "2048",
                        "uuid": "44e369cb-9174-46a4-80c7-4f15fa9bc4ad"
                    },
                    "sda2": {
                        "holders": [
                            "sysvg-root.vol",
                            "sysvg-swap.vol",
                            "sysvg-var.vol"
                        ],
                        "links": {
                            "ids": [
                                "ata-VMware_Virtual_IDE_Hard_Drive_00000000000000000001-part2",
                                "scsi-SATA_VMware_Virtual_00000000000000000001-part2"
                            ],
                            "labels": [],
                            "masters": [
                                "dm-0",
                                "dm-1",
                                "dm-2"
                            ],
                            "uuids": []
                        },
                        "sectors": "335030272",
                        "sectorsize": 512,
                        "size": "159.75 GB",
                        "start": "514048",
                        "uuid": null
                    }
                },
                "removable": "0",
                "rotational": "1",
                "sas_address": null,
                "sas_device_handle": null,
                "scheduler_mode": "cfq",
                "sectors": "335544320",
                "sectorsize": "512",
                "size": "160.00 GB",
                "support_discard": "0",
                "vendor": "ATA",
                "virtual": 1
            }
        },
        "ansible_distribution": "Imperva",
        "ansible_distribution_file_parsed": true,
        "ansible_distribution_file_path": "/etc/redhat-release",
        "ansible_distribution_file_variety": "RedHat",
        "ansible_distribution_major_version": "6",
        "ansible_distribution_release": "Final",
        "ansible_distribution_version": "6.3",
        "ansible_dns": {
            "nameservers": [
                "192.168.2.10",
                "8.8.8.8"
            ]
        },
        "ansible_domain": "localdomain6",
        "ansible_effective_group_id": 605,
        "ansible_effective_user_id": 605,
        "ansible_env": {
            "CATALINA_HOME": "/opt/apache-tomcat-8.0.33",
            "CVS_RSH": "ssh",
            "EDITOR": "vi",
            "G_BROKEN_FILENAMES": "1",
            "HOME": "/home/ansible",
            "IMPCFG_BASE": "/opt/SecureSphere/etc/impcfg",
            "IMPCFG_BIN": "/opt/SecureSphere/etc/impcfg/bin",
            "IMPCFG_ETC": "/opt/SecureSphere/etc/impcfg/etc",
            "IMPCFG_LIB": "/opt/SecureSphere/etc/impcfg/lib",
            "IMPCTL_BASE": "/opt/SecureSphere/etc/impctl",
            "IMPCTL_BIN": "/opt/SecureSphere/etc/impctl/bin",
            "IMPCTL_CFGTOOL_NAME": "impcfg",
            "IMPCTL_CTLTOOL_NAME": "impctl",
            "IMPCTL_ETC": "/opt/SecureSphere/etc/impctl/etc",
            "IMPCTL_LIB": "/opt/SecureSphere/etc/impctl/lib",
            "IMPCTL_LIBPATH": "/opt/SecureSphere/etc/impctl/lib:/opt/SecureSphere/etc/impcfg/lib",
            "IMPCTL_PRODUCT_BASE_VERSION": "",
            "IMPCTL_PRODUCT_NAME": "SecureSphere",
            "IMPCTL_PRODUCT_VERSION": "12.0.0.50_0",
            "IMPCTL_REPO_BRANCH": "v12.0_P50",
            "JAVA_HOME": "/etc/alternatives/jre",
            "LANG": "en_US.UTF-8",
            "LD_LIBRARY_PATH": "/opt/SecureSphere/server/SecureSphere/jakarta-tomcat-secsph/webapps/SecureSphere/WEB-INF/bin:/opt/oracle/ora11g/lib",
            "LESSOPEN": "|/usr/bin/lesspipe.sh %s",
            "LOGNAME": "ansible",
            "MAIL": "/var/mail/ansible",
            "MANAGEMENT_SERVER_MEMORY": "1191",
            "MANAGMENT_IP": "192.168.2.5",
            "NLS_LANG": "AMERICAN_AMERICA.AL32UTF8",
            "ONE_BOX": "false",
            "ORACLE_BASE": "/opt/oracle",
            "ORACLE_HOME": "/opt/oracle/ora11g",
            "ORACLE_SID": "secsph",
            "PATH": "/usr/lib64/qt-3.3/bin:/opt/SecureSphere/bin:/opt/SecureSphere/sbin:/opt/SecureSphere/usr/bin:/opt/SecureSphere/usr/sbin:/opt/SecureSphere/etc/impctl/bin:/bin:/sbin:/usr/bin:/usr/sbin:/usr/local/bin:/bin:/usr/bin:/opt/SecureSphere/server/bin:/opt/oracle/ora11g/bin:/opt/apache-tomcat-8.0.33/bin",
            "PCE_BASE": "/opt/SecureSphere/etc/PCE",
            "PWD": "/home/ansible",
            "PYTHONPATH": "/usr/lib64/python2.6:/opt/SecureSphere/etc/PCE",
            "QTDIR": "/usr/lib64/qt-3.3",
            "QTINC": "/usr/lib64/qt-3.3/include",
            "QTLIB": "/usr/lib64/qt-3.3/lib",
            "SECURE_SPHERE_BASE": "/opt/SecureSphere",
            "SECURE_SPHERE_DB_SAVE_AREA": "/opt/SecureSphere/db/vault",
            "SECURE_SPHERE_SERVER_BASE": "/opt/SecureSphere/server",
            "SERVER_EXPIMPTOOL_NAME": "full_expimp.sh",
            "SERVER_EXPIMPTOOL_PATH": "/opt/SecureSphere/server/bin",
            "SERVER_HOME": "/opt/SecureSphere/server",
            "SHELL": "/bin/bash",
            "SHLVL": "2",
            "SSH_CLIENT": "192.168.2.50 59620 22",
            "SSH_CONNECTION": "192.168.2.50 59620 192.168.2.5 22",
            "SSH_TTY": "/dev/pts/1",
            "STARTUP_MODE": "migration",
            "TERM": "xterm",
            "USER": "ansible",
            "_": "/usr/bin/python"
        },
        "ansible_eth0": {
            "active": true,
            "device": "eth0",
            "features": {
                "generic_receive_offload": "off",
                "generic_segmentation_offload": "on",
                "large_receive_offload": "on",
                "rx_checksumming": "on",
                "scatter_gather": "on",
                "tcp_segmentation_offload": "on",
                "tx_checksumming": "on",
                "udp_fragmentation_offload": "off"
            },
            "hw_timestamp_filters": [],
            "ipv4": {
                "address": "192.168.2.5",
                "broadcast": "192.168.2.255",
                "netmask": "255.255.255.0",
                "network": "192.168.2.0"
            },
            "ipv6": [
                {
                    "address": "fe80::20c:29ff:fe77:203d",
                    "prefix": "64",
                    "scope": "link"
                }
            ],
            "macaddress": "00:0c:29:77:20:3d",
            "module": "vmxnet3",
            "mtu": 1500,
            "pciid": "0000:03:00.0",
            "promisc": false,
            "speed": 10000,
            "timestamping": [],
            "type": "ether"
        },
        "ansible_eth1": {
            "active": false,
            "device": "eth1",
            "features": {
                "generic_receive_offload": "off",
                "generic_segmentation_offload": "on",
                "large_receive_offload": "on",
                "rx_checksumming": "on",
                "scatter_gather": "on",
                "tcp_segmentation_offload": "on",
                "tx_checksumming": "on",
                "udp_fragmentation_offload": "off"
            },
            "hw_timestamp_filters": [],
            "macaddress": "00:0c:29:77:20:47",
            "module": "vmxnet3",
            "mtu": 1500,
            "pciid": "0000:0b:00.0",
            "promisc": false,
            "timestamping": [],
            "type": "ether"
        },
        "ansible_eth2": {
            "active": false,
            "device": "eth2",
            "features": {
                "generic_receive_offload": "off",
                "generic_segmentation_offload": "on",
                "large_receive_offload": "on",
                "rx_checksumming": "on",
                "scatter_gather": "on",
                "tcp_segmentation_offload": "on",
                "tx_checksumming": "on",
                "udp_fragmentation_offload": "off"
            },
            "hw_timestamp_filters": [],
            "macaddress": "00:0c:29:77:20:51",
            "module": "vmxnet3",
            "mtu": 1500,
            "pciid": "0000:13:00.0",
            "promisc": false,
            "timestamping": [],
            "type": "ether"
        },
        "ansible_eth3": {
            "active": false,
            "device": "eth3",
            "features": {
                "generic_receive_offload": "off",
                "generic_segmentation_offload": "on",
                "large_receive_offload": "on",
                "rx_checksumming": "on",
                "scatter_gather": "on",
                "tcp_segmentation_offload": "on",
                "tx_checksumming": "on",
                "udp_fragmentation_offload": "off"
            },
            "hw_timestamp_filters": [],
            "macaddress": "00:0c:29:77:20:5b",
            "module": "vmxnet3",
            "mtu": 1500,
            "pciid": "0000:1b:00.0",
            "promisc": false,
            "timestamping": [],
            "type": "ether"
        },
        "ansible_fibre_channel_wwn": [],
        "ansible_fips": false,
        "ansible_form_factor": "Other",
        "ansible_fqdn": "localhost6.localdomain6",
        "ansible_hostname": "SecureSphereMX",
        "ansible_hostnqn": "",
        "ansible_interfaces": [
            "lo",
            "eth3",
            "eth2",
            "eth1",
            "eth0"
        ],
        "ansible_is_chroot": false,
        "ansible_iscsi_iqn": "",
        "ansible_kernel": "2.6.32-279.el6.imp7.numa.x86_64",
        "ansible_kernel_version": "#1 SMP Wed May 18 16:06:52 IDT 2016",
        "ansible_lo": {
            "active": true,
            "device": "lo",
            "features": {
                "generic_receive_offload": "off",
                "generic_segmentation_offload": "on",
                "large_receive_offload": "off",
                "rx_checksumming": "on",
                "scatter_gather": "on",
                "tcp_segmentation_offload": "on",
                "tx_checksumming": "on",
                "udp_fragmentation_offload": "off"
            },
            "hw_timestamp_filters": [],
            "ipv4": {
                "address": "127.0.0.1",
                "broadcast": "host",
                "netmask": "255.0.0.0",
                "network": "127.0.0.0"
            },
            "ipv6": [
                {
                    "address": "::1",
                    "prefix": "128",
                    "scope": "host"
                }
            ],
            "mtu": 16436,
            "promisc": false,
            "timestamping": [],
            "type": "loopback"
        },
        "ansible_local": {},
        "ansible_lsb": {
            "codename": "Final",
            "description": "Imperva release 6.3 (Final)",
            "id": "Imperva",
            "major_release": "6",
            "release": "6.3"
        },
        "ansible_machine": "x86_64",
        "ansible_memfree_mb": 3233,
        "ansible_memory_mb": {
            "nocache": {
                "free": 3643,
                "used": 191
            },
            "real": {
                "free": 3233,
                "total": 3834,
                "used": 601
            },
            "swap": {
                "cached": 0,
                "free": 3071,
                "total": 3071,
                "used": 0
            }
        },
        "ansible_memtotal_mb": 3834,
        "ansible_mounts": [
            {
                "block_available": 198259,
                "block_size": 1024,
                "block_total": 247919,
                "block_used": 49660,
                "device": "/dev/sda1",
                "fstype": "ext3",
                "inode_available": 63960,
                "inode_total": 64000,
                "inode_used": 40,
                "mount": "/boot",
                "options": "rw",
                "size_available": 203017216,
                "size_total": 253869056,
                "uuid": "44e369cb-9174-46a4-80c7-4f15fa9bc4ad"
            },
            {
                "block_available": 30338791,
                "block_size": 4096,
                "block_total": 33221470,
                "block_used": 2882679,
                "device": "/dev/mapper/sysvg-var.vol",
                "fstype": "ext3",
                "inode_available": 8435164,
                "inode_total": 8437760,
                "inode_used": 2596,
                "mount": "/var",
                "options": "rw",
                "size_available": 124267687936,
                "size_total": 136075141120,
                "uuid": "9756557e-7b49-44ef-8792-ecec9f95e37a"
            },
            {
                "block_available": 5185391,
                "block_size": 4096,
                "block_total": 7224863,
                "block_used": 2039472,
                "device": "/dev/mapper/sysvg-root.vol",
                "fstype": "ext3",
                "inode_available": 1702432,
                "inode_total": 1835008,
                "inode_used": 132576,
                "mount": "/",
                "options": "rw",
                "size_available": 21239361536,
                "size_total": 29593038848,
                "uuid": "9e7897a8-f649-4c97-8438-161256cd3865"
            }
        ],
        "ansible_nodename": "SecureSphereMX",
        "ansible_os_family": "Imperva",
        "ansible_pkg_mgr": "yum",
        "ansible_proc_cmdline": {
            "KEYBOARDTYPE": "pc",
            "KEYTABLE": "us",
            "LANG": "en_US.UTF-8",
            "SYSFONT": "latarcyrheb-sun16",
            "crashkernel": "129M@0M",
            "divider": "10",
            "notsc": true,
            "panic": "10",
            "quiet": true,
            "rd_LVM_LV": [
                "sysvg/swap.vol",
                "sysvg/root.vol"
            ],
            "rd_NO_DM": true,
            "rd_NO_LUKS": true,
            "rd_NO_MD": true,
            "rhgb": true,
            "ro": true,
            "root": "/dev/mapper/sysvg-root.vol",
            "transparent_hugepage": "never"
        },
        "ansible_processor": [
            "0",
            "GenuineIntel",
            "Intel(R) Xeon(R) CPU           X5680  @ 3.33GHz",
            "1",
            "GenuineIntel",
            "Intel(R) Xeon(R) CPU           X5680  @ 3.33GHz"
        ],
        "ansible_processor_cores": 1,
        "ansible_processor_count": 2,
        "ansible_processor_threads_per_core": 1,
        "ansible_processor_vcpus": 2,
        "ansible_product_name": "VMware Virtual Platform",
        "ansible_product_serial": "NA",
        "ansible_product_uuid": "NA",
        "ansible_product_version": "None",
        "ansible_python": {
            "executable": "/usr/bin/python",
            "has_sslcontext": false,
            "type": "CPython",
            "version": {
                "major": 2,
                "micro": 6,
                "minor": 6,
                "releaselevel": "final",
                "serial": 0
            },
            "version_info": [
                2,
                6,
                6,
                "final",
                0
            ]
        },
        "ansible_python_version": "2.6.6",
        "ansible_real_group_id": 605,
        "ansible_real_user_id": 605,
        "ansible_selinux": {
            "status": "disabled"
        },
        "ansible_selinux_python_present": true,
        "ansible_service_mgr": "upstart",
        "ansible_ssh_host_key_dsa_public": "AAAAB3NzaC1kc3MAAACBALa5y2/hJOFppDY/YqUS09EgHKjSMWhji1mnEO2X+JeVID5OzlbirkY/Hm2xhbjn+oPRKxJEO4Q+n8K/Ix7FnY0HaVim7xajpO4AUXcl8KhLGusyzIjZ0euUNT0kwf48lI79rwv09SztC+H1DLM2OCN8pEUKmIcbJ9FIND8aky0lAAAAFQCIu2gBJHDrHEKJPF0RZJkv12XB9QAAAIByDMRaXeAkQiu4oy/AE2aBkgB9aCwvPci7dbDZK4imfjdxiqp85/h4UgEpIjsgKcxnSUtg4JOBfF2/Qb/T/8re7NxH3AGGy0dWi6AX5oCL1JyDav1q1AB5umY/ZQ0h+QDXd+hHUJaCkrd7Mo3zoiL49gmhschQj2QQvwpfoD5e2QAAAIEArtCWdOv5af1pYKrP9eUpwNg7FIQsHtPWnDNUKZ16qByeZuqj7y5LqIXFRrkvwWVhJmobqxMgU0cCYVENs6zK2m5SYhvfT8PUaF81JahCydTGV+NvYzJw9E6bj3gei+F0zL03VA38kEWGTTgvAg/GHg/8RB67Ra9v2VWAJSlBXJQ=",
        "ansible_ssh_host_key_ecdsa_public": "AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBINgGUs+JRMYkljTq9Ng8I3F2Es3enSUFYE7giMg3IZYzxC/OK1bPZ8wIvkinmoMajhPDQgCCr/fUfbIcOAmjjY=",
        "ansible_ssh_host_key_ed25519_public": "AAAAC3NzaC1lZDI1NTE5AAAAIE0FeRFuDtlqLJBZtI26nqmbKVd9kWGiPAcNUfmHWRUB",
        "ansible_ssh_host_key_rsa_public": "AAAAB3NzaC1yc2EAAAADAQABAAABAQDYVbh/FsaLetPQDd9/qQ0RjSEAIejQ0Lb1R2pK1Gre0exoQKQVi6xT/8+p22Gb2RWfkmKWO6g5t3y/Jw2APReZVwis34mK3GTU3CRVHm6DcruRY1so2HsHJ86ohAIlIzRlMZnaR46QvOubxShHt+sPPBNIIf17gGYLwHTN+ONT0YhdK9Uva9kV2HOrzylMcR5/24fkd8NlXR4bE4dXbCogzSPNg8ZxMQjNN/NmTF7e9BLcaja5RQWOzx+BNf6IXQfY0z1auzbz3PmbrZ9CKeBC7/rBEM4p16mLGzwb2JBxfVFnFnBzLuA+s7RHGckxrC6NKmskkc6ciEnvojpzSsvD",
        "ansible_swapfree_mb": 3071,
        "ansible_swaptotal_mb": 3071,
        "ansible_system": "Linux",
        "ansible_system_capabilities": [
            ""
        ],
        "ansible_system_capabilities_enforced": "True",
        "ansible_system_vendor": "VMware, Inc.",
        "ansible_uptime_seconds": 37227,
        "ansible_user_dir": "/home/ansible",
        "ansible_user_gecos": "",
        "ansible_user_gid": 605,
        "ansible_user_id": "ansible",
        "ansible_user_shell": "/bin/bash",
        "ansible_user_uid": 605,
        "ansible_userspace_architecture": "x86_64",
        "ansible_userspace_bits": "64",
        "ansible_virtualization_role": "guest",
        "ansible_virtualization_type": "VMware",
        "discovered_interpreter_python": "/usr/bin/python",
        "gather_subset": [
            "all"
        ],
        "module_setup": true
    },
    "changed": false

