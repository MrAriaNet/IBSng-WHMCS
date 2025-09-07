# IBSng WHMCS Module

![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)
![WHMCS Compatible](https://img.shields.io/badge/WHMCS-Compatible-brightgreen.svg)
![Version](https://img.shields.io/badge/Version-1.0.0-blueviolet.svg)

A **WHMCS module** for managing **IBSng** accounts, including password changes and full integration with WHMCS.  

---

## Features

- Change user passwords in IBSng directly from WHMCS  
- Complete logging of IBSng responses for debugging  
- Securely update user passwords in WHMCS  
- Display real IBSng errors instead of generic "Unknown Error"  
- Compatible with both older and newer versions of WHMCS  

---

## Installation

1. Place the module files in your WHMCS installation:

```
/modules/servers/ibsng/
````

2. In WHMCS admin panel:  
**Setup → Products/Services → Servers → Add New Server**, select **IBSng** as the server type.

3. Configure the server:  
   - IBSng server IP  
   - Username and password  
   - Other settings according to your setup  

---

## Usage

- Users can change their passwords from the **Client Area**.  
- Admins can manage user accounts and passwords from the **Admin Area**.  

---

## Important Notes

- Ensure the `templates_c` directory in `/usr/local/IBSng/interface/smarty/` exists and is writable:

```bash
mkdir -p /usr/local/IBSng/interface/smarty/templates_c
chown -R apache:apache /usr/local/IBSng/interface/smarty/templates_c
chmod -R 755 /usr/local/IBSng/interface/smarty/templates_c
````

* For older WHMCS versions (<8.x), use the global `encrypt()` function for password encryption.

* All IBSng responses are logged to `/tmp/ibsng_full_response.log` for debugging purposes.

---

## Acknowledgements

Thanks to [miladworkshop](https://github.com/miladworkshop/whmcs-ibsng) for releasing the original source code, which served as the foundation for this module.

---

## License

This module is released under the **MIT License**.
