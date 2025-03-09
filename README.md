🌍 Assets
Use the following URL pattern to load assets from this repository. Simply replace "path-to-file" with the desired file name:

https://raw.githubusercontent.com/janibehm/assets/main/assets/path-to-file
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
