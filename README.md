# bastion-icons

Bastion UI SVG icons

## Usage

```ts
import Bast from '@bs-solutions/bastion-icons/icons-common/bast.svg';
```

## React SVGR+VITE

```tsx
import Bast from '@bs-solutions/bastion-icons/icons-common/bast.svg?react';
import { BastHeader } from '@bs-solutions/bastion-ui';

export const Header: FC<THeaderProps> = ({ title, icon }) => (
    <BastHeader fluid className='p-1 header'>
        <div className='c-white header__content'>
            <div className='header__title mr-2'>
                <Bast />
            </div>
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
