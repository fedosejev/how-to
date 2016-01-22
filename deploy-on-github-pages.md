# How to deploy your static website on GitHub Pages?

### Step 0: GitHub
1. Create a new GitHub repository and clone it.
2. Add all your source files, including `index.html`.
3. Commit and push: `git add . && git commit -m "Add source files" && git push`

### Step 1: GitHub Pages

1. Create `gh-pages` branch: `git checkout -b gh-pages && git push origin gh-pages`.
2. Create `CNAME` file with your domain name in it, e.g.: `yourdomainname.com`: `touch CNAME && echo yourdomainname.com > CNAME`
3. Create `.nojekyll` file: `touch .nojekyll`
4. Commit and push: `git add . && git commit -m "Add custom domain" && git push`

### Step 2: Domain Name System

1. Login to your domain name registrator, such as [NameCheap](https://www.namecheap.com), [GoDaddy](http://godaddy.com), [IWantMyName](http://iwantmyname.com), etc.
2. Select the domain name that you want to use with your GitHub Pages and choose to edit its DNS settings.
3. Add `A` record:
  + Hostname: `@`
  + Type: `A`
  + Value: `192.30.252.153`
  + TTL: `900`
4. Add another `A` record:
  + Hostname: `@`
  + Type: `A`
  + Value: `192.30.252.154`
  + TTL: `900`

### Step 3: Test!

1. Go to your GitHub repository's settings and make sure that it says: `Your site is published at http://yourdomainname.com.`
2. Open `http://yourdomainname.com` in a web browser - check that everything loads!



