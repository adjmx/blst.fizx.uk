# blst.fizx.uk

> Nostr event rebroadcaster — push any event across an arbitrary relay list.

**Live**: <https://blst.fizx.uk>

## Stack

- [Vite](https://vitejs.dev/) + React 18 + TypeScript
- Tailwind CSS
- [nostr-tools](https://github.com/nbd-wtf/nostr-tools)
- lucide-react

## Nostr

- **Login**: NIP-07 (browser extension) + NIP-55 (Amber callback URI)
- `any kind` — user-selectable — kinds 0/1/3/4/5/6/7/8/9/30023/etc

Default target relay: `wss://git.upleb.uk` (the upleb GRASP relay).

## Develop

```bash
npm install
npm run dev
```

## Build + deploy

```bash
npm run build
rsync -avz --delete -e "ssh -p 2121" dist/ root@88.218.206.187:/var/www/blst.fizx.uk/
```

VPS: `88.218.206.187`. Full server / nginx / SSL / DNS notes for the wider deployment live in the local `code_vibe/CLAUDE.md` (not pushed; this README is the public-facing summary).

---

_Sister repo on the other side: <https://github.com/macos-node/blst.upleb.uk>_
