

# ScoreApp TestFlight

## Manual

1. In Terminal, Git pull Flutter project

2. In VS Code,

   a. Check ios/Podfile, use this line

   ```
   platform :ios, '12.0'
   ```

   <img src="screenshot1.png" alt="Screenshot" style="zoom:30%;" />

   b. Check ios/Flutter/AppFrameworkInfo.plist, use 12.0 for MinimumOSVersion

   ```
   <key>MinimumOSVersion</key>
   <string>12.0</string>
   ```

   <img src="screenshot2.png" alt="Screenshot" style="zoom:33%;" />

3. In Terminal,

   ```shell
   cd ios
   pod install
   ```

   ![Screenshot](screenshot3.png)

4. In Browser, login https://developer.apple.com/

   Click Account

   <img src="screenshot4.png" alt="Screenshot" style="zoom:33%;" />

   

   Click Certificates, Identifiers & Profiles

   <img src="screenshot5.png" alt="Screenshot" style="zoom:33%;" />

   

   Click (+)

   <img src="screenshot6.png" alt="Screenshot" style="zoom:33%;" />

   

   Select App IDs > Continue

   <img src="screenshot7.png" alt="Screenshot" style="zoom:33%;" />

   

   Select App > Continue

   <img src="screenshot8.png" alt="Screenshot" style="zoom:33%;" />

   

   Fill in Description > Choose Explicit for Bundle ID > Fill in explicit ID > Tick needed Capabilities > Continue

   <img src="screenshot9.png" alt="Screenshot" style="zoom:33%;" />

   

   Click Register

   ![Screenshot](screenshot10.png)

5. In browser, login https://appstoreconnect.apple.com/

   Click My Apps> (+) > Choose New App>Tick iOS >Fill in Name>Choose Primary Language> Choose the Bundle ID just  created > Fill in SKU> Choose Full Access for User Access> Click Create

6. In Finder, browse folder /ios, double click Runner.xcworkspace

   In Xcode, 

   a. Click File>Workspace Settings>Choose "Legacy Build System" for "Build System"> Done

   b. On left side, click Runner Project> click Runner under TARGETS> click General tab

   c. In Identity, Fill in Bundle Identifier with Bundle ID just created before

   d. In Deployment Info, choose Target iOS version

   e. Click Signing & Capabilities, choose Team with correct Apple Developer Account> Bundle Identifier should be already same as what you have filled > show no error

   f. Click Run>should show build succeeded

7. In Xcode, Click Product on top>Archive> wait until it finishes loading> should show build succeeded> Click Distribiute App>Choose App Store Connect>Next>Choose Upload>Next>Tick Strip Swift symbols and tick Upload your app's symbols..... >Upload>Done

8. In browser, in App Store Connect, 

   a. Click My Apps> click my newly created app>Click TestFlight>Click Test Information on the left>Fill in Beta App Description, Feedback Email, Marketing URL, Privacy Policy URL, First Name, Last Name, Phone number, Email, Review Notes and License Agreement> no need to tick Sign-in required> Save> the yellow question mark should disappear

   b. Click iOS on the left> click Manage behind "Missing Compliance">Choose No for the encryption question> Click Start Internal Testing

   c. If apple users were not added, click **Users and Access** on top > (+)> Fill in info> Invite > Wait apple user accept through email

   c. Click App Store Connect Users on the left> (+)> tick users > Add

   

