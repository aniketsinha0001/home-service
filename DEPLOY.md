# Deploying the Call It Home website

This is a static site: plain HTML, images and one logo. It needs no database or server software. Upload the whole folder (keep `index.html` at the top level next to `images/` and `assets/`).

## Folder contents

| Item | Purpose |
|---|---|
| `index.html` | The whole homepage (styles and scripts included) |
| `images/` | Your 15 design renders |
| `assets/` | Logo, business card image, favicon |
| `robots.txt`, `sitemap.xml` | Basic search engine files (assume `https://www.callithome.in/`) |

## Option A: Netlify (easiest, free plan available)

1. Unzip the download on your computer.
2. Go to https://app.netlify.com/drop and sign up or log in.
3. Drag the unzipped `callithome-website` folder onto the page. Your site goes live on a temporary `something.netlify.app` address within a minute. Open it and check it.
4. In the site's dashboard open **Domain management** (labels may vary slightly), choose **Add a domain**, and enter `callithome.in`.
5. Netlify shows the DNS settings to use. You have two ways to apply them:
   - **Use Netlify DNS:** change the nameservers at your domain registrar to the ones Netlify lists. Simplest, but it moves all DNS (including any email records) to Netlify.
   - **Keep your registrar's DNS:** at the registrar, add the records Netlify shows. This is usually an `A` record for `callithome.in` and a `CNAME` record for `www` pointing to your `.netlify.app` address. Copy the exact values from Netlify, because they can change.
6. Wait for DNS to update (often under an hour, sometimes up to 24 hours). Netlify then issues the free HTTPS certificate automatically. Pick whether `callithome.in` or `www.callithome.in` is the main address, and Netlify redirects the other.

To update the site later, drag the updated folder onto the site's **Deploys** tab.

## Option B: Existing web hosting with cPanel (GoDaddy, Hostinger, BigRock and similar)

1. Log in to your hosting control panel and open **File Manager**.
2. Open the `public_html` folder (or the folder your domain points to).
3. Upload `callithome-website.zip` and use **Extract**. Move the extracted files so `index.html` sits directly inside `public_html`, not inside a sub-folder.
4. Make sure the domain's nameservers or A record point to this hosting account. Your host's welcome email lists them.
5. Turn on HTTPS: look for **SSL/TLS** or **AutoSSL** (or "Free SSL") in the panel and enable it for `callithome.in` and `www.callithome.in`.
6. Visit `https://www.callithome.in` and refresh with Ctrl+F5 if you see an old page.

## Option C: Cloudflare Pages or GitHub Pages

Both are free and work the same way: create a project, upload or push this folder, then add `callithome.in` as a custom domain and follow the DNS steps the dashboard shows.

## After it is live: checklist

1. Open the site on your phone. Tap **Book on WhatsApp** and confirm the chat opens to +91 86187 31376 with the message filled in.
2. Fill the contact form and test both **Send on WhatsApp** and **Send by email**.
3. Replace the three sample reviews (search `index.html` for `Sample text`) with real client reviews and remove those tags.
4. Add `https://www.callithome.in` to your Instagram bio and, if you have one, your Google Business Profile.
5. Optional: submit the site at https://search.google.com/search-console so Google finds it sooner.

## Editing tips

- **Text:** open `index.html` in any text editor (Notepad, VS Code) and change the words between the tags.
- **Photos:** keep each image around 1280 pixels wide and under 300 KB. Save it into `images/`, then copy one of the existing `<button class="shot">` lines in the portfolio section and change the file name, caption and category (`living`, `pooja`, `kitchen` or `bed`).
- **Phone or email:** search for `918618731376` and `callithome3@gmail.com` and change every match.
