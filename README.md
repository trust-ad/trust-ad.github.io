### TrustDrive: Data-Driven Simulations for Safe and Trustworthy Autonomous Driving
Workshop website template

## Build
1. Install [Hugo](https://gohugo.io/)
2. Clone the repo
```
git clone https://github.com/trust-ad/trust-ad.github.io.git
cd trust-ad.github.io
```
3. Run `hugo` in the `pwd`. This will build the website locally
4. To watch on localhost, run `hugo server --watch`. This is will give a localhost link.

## Adding Data
1. `index.html` in `layout/` is to be edited/changed.
2. `index.html` in `static/categories` is to be edited/changed. Replace the ml4ad with our website.
3. Adding the images content in `static/img`.
4. `index.html` in `static/tags` is to be edited/changed. Replace the ml4ad with our website.

## Deploying
`Note: Verify locally first and then push to github`

1. Run `hugo` in `pwd`, after editing the files. This will generate the `public` folder, which is then used for the deployment.
2. Steps to push local data to the remote
```
git checkout main
git add .
git commit -m " updated"
git push origin main
```
3. We are using `gh-pages` for the deployment.
```
git checkout  gh-pages
git fetch origin gh-pages
git rm -rf .
git checkout main -- 'public/*'
mv -f public/* .
rm -r public
git add .
git commit -m "updated"
git push origin gh-pages
```
4. The website will be live with the changes at [https://trust-ad.github.io/]