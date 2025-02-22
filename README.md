![image](https://github.com/user-attachments/assets/dd996920-23dc-44d5-a52a-caa67b5276b6)


## Disclaimer: This is in beta! Use this app at your own risk! Please use the pop-out feature when making large trades: 
![image](https://github.com/user-attachments/assets/6bccf77e-1665-483a-829d-fefcc5d5fb09)


# Usage
This is an experimental web app designed to trade with multiple dexes in one place. Intensive trading often requires multiple windows or monitors to have an effective edge, ShellOS is designed to organize this all in one place in an optimized manner.

# Setup

-npm install @ source directory
-npm run dev to run it locally

# known issues/notes

-some dapps don't like this style of embedding, icpswap and kong require a proxy server to access. coming soon TM until a sandbox is made.

-Uniswap and jupiter may have issues on mobile, desktop has worked better in my tests. This also may be browser dependant, if you run into issues more often than not using another browser can help.

-For mobile use, I recommend a max of 2-3 tabs. Optimizing this further slows down the experience for more powerful devices.

# Fixes

- Fixed issues with tabs and window management. Switching between tabs and all that now works as intended. The main window X button will only close the tab you're in, unless users want this changed I will keep this as is.

# For devs

ShellOS is lightwieght (main component is 780 lines including spacing) and was made in nextjs 15 + react 19. You can add this entire app to your app by adding "MagicLaucher" in a self-closing tag to your page.tsx or other main component file. The design of having this entire app in a single component is highly questionable, however this may be changed.

# How to add or remove apps

1. Ctrl + F and search for "add more sites here"
2. Scroll to the bottom of the const variable until you see the final app (id 10 at the time of writing this)
3. Copy and paste the following code after the final entry
   ```
   {
      id: [ENTER ID NUMBER],
      title: "[ENTER APP NAME]",
      description: "[ENTER APP DESCRIPTION]",
      url: "[PASTE DAPP URL]"
   },
   ```
5. Change the id to be +1 of the final ID (ig. if the final id is 10, change this entry to 11)
6. Add your name, description, and URL.
7. That's it! You should see the website added automatically once you save the file.

Note: If you add a dapp and see a 404 or "can't access this page". This is a policy on the website blocking connection to prevent bots. This requires a proxy server to bypass or another integration method to specially bypass this. This has not been added as of yet and is being considered for future iterations.
