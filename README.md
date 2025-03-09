��#   a s s e t s 
 
Use this url pattern to load the asset. Just change the "path-to-file" to one you want to use.

https://raw.githubusercontent.com/janibehm/assets/main/assets/environment.jpg";

Example how to load on javascript.

	// Load environment texture with error handling
	const envTexturePromise = new TextureLoader()
		.loadAsync('https://raw.githubusercontent.com/janibehm/assets/main/assets/environment.jpg')
		.then((texture) => {
			texture.mapping = EquirectangularReflectionMapping;
			return texture;
		})
		.catch((error) => {
			console.warn('Failed to load environment texture:', error);
			return null; // Return null to handle the error gracefully
		});
