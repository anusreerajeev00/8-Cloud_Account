# Steps Followed (Azure CLI Alternative Path)

## Provider chosen
Microsoft Azure (Azure CLI on Linux)

---

## A) Authenticate via CLI
1. Opened terminal in Linux.
2. Run the device-code login command:
   - `az login --use-device-code`
3. Azure CLI displayed a login URL and one-time code.
4. Since I could not create my own cloud account, I followed the alternative method:
   - A peer (batchmate) approved the device-code login from their browser.
   - No passwords or secret credentials were shared.
5. Selected the required subscription when prompted.

---

## B) Discover basic account context
1. Checked the active account and subscription:
   - `az account show`
2. Listed available subscriptions:
   - `az account list --output table`
3. Listed available Azure locations:
   - `az account list-locations --output table`

---

## C) List cloud resources
1. Listed resource groups:
   - `az group list --output table`
2. Listed all resources in the subscription:
   - `az resource list --output table`
3. Listed Azure providers/services:
   - `az provider list --output table`

---

## D) Create and clean up a resource group
1. Created a resource group:
   - `az group create --name <group_name> --location <available_location>`
2. Verified the resource group exists:
   - `az group show --name <group_name>`
3. Deleted the created resource group:
   - `az group delete --name <grup_name> --yes --no-wait`
4. Confirmed the resource group was deleted:
   - `az group list --output table`
