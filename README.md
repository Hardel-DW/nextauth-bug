# nextauth-bug

# Setup
1. Rename exemple.env to .env file
2. Add Providers Client and Secret
3. use yarn
4. start the project with next dev

# Reproduce bug :
1. Setup project and start the project
2 (A). Go to localhost:3000/api/auth/signin. See the error
2 (B) - Use unstable_getServerSession see tje Json Parse error.

"Error: This action with HTTP GET is not supported by NextAuth.js"

# Problem
Define "NEXTAUTH_URL" in developpement cause this error, if you remove this "env" entry the routes nextauth works.

# Note
The most surprising thing is that I have been working with this line in my .env file for two months
And only since I did "rm -rf ./node_modules/" with a clean reinstallation "yarn" or "npm i" I have this error.
