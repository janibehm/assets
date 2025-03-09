🌍 Assets
Use the following URL pattern to load assets from this repository. Simply replace "path-to-file" with the desired file name:

https://raw.githubusercontent.com/janibehm/assets/main/assets/path-to-file

You can load assets from https://polyhaven.com/

When you want to load assets from your local environmet to this repository make sure to 

Example: Load an Environment Texture in JavaScript

import { TextureLoader, EquirectangularReflectionMapping } from 'three';

// Load environment texture with error handling

const envTexturePromise = new TextureLoader()
  .loadAsync('https://raw.githubusercontent.com/janibehm/assets/main/assets/environment.jpg')
  .then((texture) => {
    texture.mapping = EquirectangularReflectionMapping;
    return texture;
  })
  .catch((error) => {
    console.warn('Failed to load environment texture:', error);
    return null; // Handle the error gracefully
  });

🚀 How to Push Changes Without Overwriting Anything
Follow these steps to safely push your changes while ensuring you don’t overwrite existing work.

1. Pull the Latest Changes (Important)
Before pushing, always pull the latest changes from GitHub to prevent overwriting:

git pull origin main --rebase  # Replace 'main' with your branch if needed

3. Stage Your Changes
Add all new, modified, and deleted files to the next commit:

git add .

3. Commit Your Changes
Save your changes with a meaningful commit message:

git commit -m "Describe your changes here"

4. Push Your Changes to GitHub
Now, push your updates without overwriting anything:

git push origin main

5. Handling Merge Conflicts (If Needed)
   
If you encounter conflicts during git pull, manually resolve them, then run:

git add .
git rebase --continue
git push origin main

⚠ Avoid using git push --force, as it can overwrite others’ work!

This ensures your commits are safe, conflict-free, and up to date. 🚀
