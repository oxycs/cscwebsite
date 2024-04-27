# Computer Science Club Website
 
This website is made using SvelteKit.

To run the website locally, run the following commands after cloning:

```bash
cd cscwebsite
npm install
npm run dev -- --open
```

To add a page, create a new folder in the `src/routes` directory. The name of the folder will be the name of the page. Inside the folder, create a `+page.svelte` file. This file will be the content of the page.

If the page needs to be added to the navigation bar, edit `src/lib/components/borger.svelte` in both the `full` and `expanded` sections.

You can use HTML, CSS, and JavaScript in the `+page.svelte` file. You can also use Svelte components. Take a look at  existing pages for inspiration.

Images, fonts, and other assets can be placed in the `static` directory.

---
### Deployment

To deploy the website on the main server, run the following command:

```bash
sudo docker run -p 8080:8080 --name website --network nginx_default -itd $(sudo docker build -q .)
```

This will compile the website into an image, and automatically run it in a container.
The container will be named "website", and it will be networked to the nginx installation. It will also expose port 8080.

Once deployed to the server, you can access it via `https://csc.oxy.edu` publicly, or `http://oxycsc:8080` via Tailscale.

To update the server after a git push, run the following command in the `cscwebsite` directory on the server:

```bash
git pull && sudo docker stop website && sudo docker rm website && sudo docker run -p 8902:8080 --name website --network nginx_default -itd $(sudo docker build -q .)
```