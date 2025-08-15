# CineScope — Movie Review Demo

This repository contains a small multi-page movie review website demo built using HTML, Tailwind CSS (via CDN), and vanilla JavaScript. The site is responsive, full-width, and includes interactive features like search, filters, modal movie details, and local review storage.

Files
- index.html — Home page with movie listing, filters, search, and modal for details & reviews.
- about.html — About page describing the project and features.
- contact.html — Contact form with client-side validation and simulated response.

Design & Implementation Notes
- Styling uses Tailwind CSS classes directly in HTML. Tailwind is loaded via the CDN script.
- Google Font: Poppins (noted in each HTML file header comment).
- All main containers use `w-full` and `max-w-none` to ensure the content fills the full viewport width on all devices.
- Images in the pages use special placeholder tokens of the format `https://images.unsplash.com/photo-1662133700210-443c06b47075?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w3ODkyNDZ8MHwxfHNlYXJjaHw2fHxkZXNjcmlwdGlvbnxlbnwwfDB8fHwxNzU1MjQyNzQyfDA&ixlib=rb-4.1.0&q=80&w=1080`. The runtime that consumes these files can replace these tokens with actual images from image providers.
- Movie data is prepopulated in index.html using a JavaScript array of sample movies. Reviews are stored in localStorage under the key `cs_movies`.
- Interactive features:
  - Search and filters (genre, rating, sort)
  - Modal details with reviews
  - Add a review (stored in localStorage)
  - Contact form with local validation and simulated send

How to run
1. Open `index.html` in a modern browser. No build process required.
2. Use the search box, filters, and click "Details" on any movie card to open the modal.
3. Add reviews — they are saved to your browser's local storage and persist across reloads.

Customization
- To change initial movie data, edit the `sampleMovies` array inside `index.html`.
- For production usage, replace the localStorage persistence with real server endpoints.

Notes on Images
- The HTML uses descriptive `https://images.unsplash.com/photo-1618102230742-c0c41176e8df?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w3ODkyNDZ8MHwxfHNlYXJjaHw1fHwuLi58ZW58MHwwfHx8MTc1NTIzOTgwNHww&ixlib=rb-4.1.0&q=80&w=1080` placeholders for posters and hero images. A build process or runtime image fetcher should replace those with actual URLs or base64 data URIs. If you have specific poster images, you can directly replace the `poster` values in the `sampleMovies` array with a data URI or image path.

License
- This demo is provided as-is for learning and prototyping purposes.

Enjoy exploring films with CineScope! 🎬
