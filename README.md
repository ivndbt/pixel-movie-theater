# Pixel Movie Theater

Read the poster rules on the [website](https://sitopage.com/nomerepo/#join) before you start.

## Naming and formatting

- Name your file like this: `film-title-username.png` or `.gif` (lowercase, words separated by hyphens, no spaces).
- Keep the same indentation as the other poster blocks in `index.html`.

## How to submit - coding version

```sh
git clone https://github.com/your-username/this-repo.git
cd this-repo
git switch -c add-film-title
# add posters/film-title-username.png
# add the <figure> block at the top of the .wall div in index.html, above the other posters
git add .
git commit -m "Add Film Title"
git push -u origin add-film-title
```

Then open a pull request from your fork. Read the whole checklist in its description and make sure you did everything correctly before submitting.

### Another poster

Sync your fork with the original repository before starting a new branch.

```sh
# only the first time: add the original repository as "upstream"
git remote add upstream https://github.com/ORIGINAL-OWNER/this-repo.git

# every time
git switch main
git pull upstream main
git push origin main
git switch -c add-another-film-title
```

Then repeat the steps above: add your poster, commit, `git push -u origin add-another-film-title` and open a pull request.

## How to submit - no coding alternative

Everything below happens in your browser on github.com.

### 1. Fork this repository

A fork is your own copy of the project where you can make changes safely.

1. Click **Fork** at the top right of this page.
2. Click **Create fork**.

You are now on your copy at `github.com/your-username/...`.

### 2. Create a branch

A branch keeps your changes separate from the rest of the project.

1. Click the button that says **main** (top left above the file list).
2. Type a name like `add-film-title` (lowercase, hyphens, no spaces).
3. Click **Create branch add-film-title from main**.

Make sure the button now says `add-film-title`. All the next steps must happen on this branch.

### 3. Upload your poster

1. Open the `posters` folder.
2. Click **Add file** > **Upload files**.
3. Drag your poster in (or click *choose your files*).
4. Under *Commit changes* write a short message like `Add poster for Film Title`.
5. Select **Commit directly to the add-film-title branch**, then click **Commit changes**.

### 4. Add your poster to the page

1. Go back to the root of your fork (check that the branch button still says `add-film-title`) and click `index.html`.
2. Click the **pencil icon** at the top right of the file (*Edit this file*).
3. Find the comment `<!-- Paste your poster below this line, above the other figures -->` near the top of the poster list (press `Ctrl+F` / `Cmd+F` to search for "Paste your poster").
4. Put your cursor at the end of that comment line, press Enter twice, and paste this:

```html
<figure class="poster">
  <img loading="lazy" src="posters/film-title-username.png" alt="">
  <figcaption>
    Film Title
    <small>2026</small>
    <em><a href="https://your-website.com/">username</a></em>
  </figcaption>
</figure>
```
> Don't delete the comment.

5. Edit the pasted block:
   - `src`: the exact name of the file you uploaded.
   - `Film Title`: the movie title.
   - `2026`: the release year.
   - `https://your-website.com/`: your website.
   - `username`: the name you wnat shown on the plate.
6. Click **Commit changes...** (top right), write a message like `Add Film Title to the corridor`, select **Commit directly to the add-film-title branch** and confirm.

> Careful: only change the lines above and keep the rest of the file untouched.
> If something looks wrong, click **Cancel changes** and start again.

### 5. Open a pull request

A pull request is how you ask me to add your changes to the main project.

1. Go to the main page of your fork. A yellow banner shows your branch: click **Compare & pull request**.
   (No banner? Open the **Pull requests** tab > **New pull request**, and pick your branch on the right.)
2. Give it a title like `Add Film Title by username`.
3. The description comes with a checklist. Read all of it and make sure you did everything correctly, then tick each item.
4. Click **Create pull request**.

That's it! I'll review your submission. If something needs fixing I'll leave a comment on the pull request, and you can fix it by editing the files on the same branch (the pull request updates by itself).
Once merged, your poster will appear in the corridor within a few minutes.

If GitHub says there are **conflicts**, don't worry: it just means someone else added a poster at the same time. I'll fix it or let you know what to do.

### Submitting another poster

Go to your fork, click **Sync fork** > **Update branch** (on `main`), then start again from step 2 with a new branch name.

## Need help?

Open an [issue](../../issues) and tell me where you got stuck.