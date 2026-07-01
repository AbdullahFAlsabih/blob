# blob

I have implemented the core C interfaces for safe, boundary-checked manipulation of binary large objects (blobs). These functions handle internal cursor navigation as well as reading and writing data at specific offsets.

API Overview
All functions return a bool indicating success (true) or failure/out-of-bounds (false), ensuring memory-safe operations.

blb_blob_jump(blb_blob_t *blob, int32_t value)
Moves the blob's internal cursor forward (positive value) or backward (negative value).

blb_blob_block_put(blb_blob_t *blob, int32_t offset, uint8_t value)
Safely writes a single byte (value) to the specified offset within the blob.

blb_blob_block_get(blb_blob_t *blob, int32_t offset, uint8_t *value)
Safely reads a single byte from the specified offset and stores it in the provided *value pointer.
