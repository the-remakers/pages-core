---
layout: page
title: Rust WASM Test
description: Navigate through interconnected challenges in a satellite communication network
permalink: /digital-famine/microblog/wasm-test
breadcrumb: true
---

<script type="module">
    import init, { add } from 'https://the-remakers.github.io/rust-wasm-libs/pkg/crypto_utils/crypto_utils.js';

    async function run() {
        try {
        // Initialize the WASM module
        await init('https://the-remakers.github.io/rust-wasm-libs/pkg/crypto_utils/crypto_utils_bg.wasm');

        // Now you can use exported functions
        const sum = add(1, 2);
        console.log('1 + 2 =', sum);
        } catch (e) {
        console.error('WASM initialization failed:', e);
        }
    }

    run();
</script>