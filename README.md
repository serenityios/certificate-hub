# Certificate Hub

Welcome to the **Certificate Hub** — a centralized location where we store all the `.p12` certificates and `.mobileprovision` profiles used for signing iOS apps in Serenity.

## Why Do We Store Certificates Here?

The certificates are stored in this hub for a very important reason: **we need a valid URL to save to the browser's local storage** in order for `.ipa` signing to work properly.

### How It Works:
1. **Select a Certificate** from the Certificate Hub:
   - This action replaces the `mp`, `p12`, and `password` values in your browser's local storage.
   
2. **Access Local Storage via PHP** inside the app:
   - The app fetches the values from local storage and uses `wget` to download the `.p12` and `.mobileprovision` files.
   - The associated password is also retrieved.

3. **Sign the App**:
   - With the required files and password, the app is signed successfully.

## Are These Serenity's Certificates?

**No**, we do not use Serenity's own certificates. Instead, we find **Enterprise Certificates** that are available online, especially from sources like **AppleP12.com** or **CookHub**.

## Can I Use or Distribute These Certificates?

Yes, **as long as it's not for any fraudulent or scamming activities**. The certificates are intended for legitimate use only.

---
For any additional questions or concerns, feel free to contact us!
