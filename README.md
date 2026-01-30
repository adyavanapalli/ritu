# RITU

**R**edirect **I**ntent **T**o **U**PI

Turns HTTPS links into `upi://` deep links that open UPI apps directly.

Live at [payviaupi.link](https://payviaupi.link).

## Usage

Construct a link with query parameters:

```
https://payviaupi.link/pay?pa=ritu@ybl&pn=Ritu&am=50&tn=coffee
```

When opened on a phone, the user taps "Pay via UPI" and their UPI app opens with the details pre-filled.

### Parameters

| Param | Description                    |
| ----- | ------------------------------ |
| `pa`  | Payee UPI address (e.g. `ritu@ybl`) |
| `pn`  | Payee name                     |
| `am`  | Amount (up to 2 decimal places) |
| `tn`  | Transaction note (max 80 chars) |

## Tech Stack

- [SvelteKit](https://svelte.dev/docs/kit) + [Svelte 5](https://svelte.dev)
- [Tailwind CSS v4](https://tailwindcss.com) with [Catppuccin Mocha](https://catppuccin.com) theme
- Deployed on [Cloudflare Pages](https://pages.cloudflare.com) via `@sveltejs/adapter-cloudflare`

## Development

```sh
npm install
npm run dev
```

## Build

```sh
npm run build
```

## License

[MIT](LICENSE)
