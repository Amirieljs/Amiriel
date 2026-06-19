# Amiriel

Portable Vue 3 body editor and renderer for Amiriel letters.

## Install

```bash
pnpm add amiriel
```

## Usage

```vue
<script setup lang="ts">
import { ref } from "vue";
import { AmirielBodyEditor, AmirielBodyRenderer, type AmirielDocument, type AmirielMediaRequest } from "amiriel";
import "amiriel/style.css";

const document = ref<AmirielDocument>({
  theme: "midnight",
  media: [],
  pages: [{ id: "page-1", order: 0, text: "", font: "handwritten", mediaIds: [], mediaPlacements: [], textBlocks: [] }],
});

async function onMediaRequest(request: AmirielMediaRequest) {
  request.handled = true;
  try {
    const media = await uploadMediaSomewhere(request.file);
    request.resolve(media);
  } catch (error) {
    request.reject(error instanceof Error ? error.message : "Upload failed");
  }
}
</script>

<template>
  <AmirielBodyEditor v-model="document" locale="en" @media-request="onMediaRequest" />
  <AmirielBodyRenderer :document="document" locale="en" />
</template>
```

The package does not include storage, authentication, database code, or application workflow. Host apps own media upload and pass the resulting media object back through `request.resolve(media)`.

## License

[MIT](./LICENSE)
