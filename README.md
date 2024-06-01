# Trendloom

## How to Deploy Locally

### API:

- Make sure to install vendor packages by running `composer install`.
- Execute `php artisan app:init` once to refresh and seed the database with mock data.
- Launch the Laravel server using Laragon. Then proceed with the steps for the app below.

### APP:

- Ensure node modules are installed with `npm install`.
- Start the local server with `npm run dev` to access the webshop app.
- (Optional) Confirm that your `mkcert` is configured for secure localhost; authentication requires it.

## Implemented Features

### API:

- Fetch detail.
- Fetch a list with paging.
- Add, update, and delete an entry.
- Translation support.

### APP:

#### BACKOFFICE:

- Display a list of entries (products, categories, brands are implemented).
- View details of an entry (categories and brands are implemented, serves as the edit screen since it contains the details of an entry)
- Search and filter the list (on the product page, you can search and filter products after a debouncing time for optimized fetching calls).
- Add, update, and delete an entry (you can add and update categories and brands, and delete products, brands, and categories).

#### FRONTEND:

- Show a list of entries translated into one language (e.g., products, brands, shopping cart items).
- Show details of an entry translated into one language.
- Search and filter the list (filter by parameters such as itemCount and sort; sorting options include price ascending, descending, newest, or default).
- Option to switch languages (in the navbar, click the language icon to open a modal and switch between currently available languages in the database).
- Authentication via JWT - login and registration (register and log in securely via these pages; authentication is handled via JWT).

## Not Implemented Features

- Image/file upload (due to time constraints from other projects).

## Known Bugs

- **Non-breaking UI bug:** When adding a product to your shopping cart without an open order, the shopping cart UI sometimes fails to refresh immediately. Refreshing the browser resolves this, displaying the added product. Subsequent additions to an open order (status = shopping) update the UI instantly, providing a seamless experience.
