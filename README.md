# bastion-icons

Bastion UI SVG icons

## Usage

```ts
import Bast from '@bs-solutions/bastion-icons/bastion/bastion-logo-full.svg?react';
```

## React SVGR+VITE

```tsx
import Bast from '@bs-solutions/bastion-icons/bastion/bastion-logo-full.svg?react';
import { BastHeader } from '@bs-solutions/bastion-ui';

export const Header: FC<THeaderProps> = ({ title, icon }) => (
    <BastHeader logo={Bast} fluid className='p-1 header'>
        <div className='c-white header__content'>
            <ContextMenu />
        </div>
    </BastHeader>
);
```
### vite.config.ts:
```ts
import react from '@vitejs/plugin-react';
import svgr from 'vite-plugin-svgr';
import { defineConfig, loadEnv } from 'vite';

// https://vite.dev/config/
export default defineConfig(({ mode }) => {
  const env = loadEnv(mode, process.cwd());

  return {
    plugins: [react(), svgr()],
  };
});
```

## Publish
```bash
  npm run publish
```
