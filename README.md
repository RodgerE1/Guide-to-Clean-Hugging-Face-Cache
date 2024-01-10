
# How to Clean Your Hugging Face Cache Efficiently

Hey everyone! If you're using Hugging Face's amazing libraries and tools, you might have noticed that over time, your cache can grow quite large. Here's a simple guide on how to clean up your Hugging Face cache using their CLI tools, as detailed in their official documentation.

## Step 1: Install the Hugging Face CLI

First, make sure you have the Hugging Face CLI installed. You can do this by running:

```bash
pip install huggingface-hub
```

## Step 2: Understanding Your Cache

Before cleaning, it's a good idea to understand what's in your cache. You can scan and get a report on your cache by running:

```bash
huggingface-cli scan-cache
```

This command provides a detailed overview of the cached models and datasets, including size, number of files, and more.

## Step 3: Cleaning the Cache

To clean your cache, Hugging Face offers several methods. One of the easiest ways is to use the `delete-revisions` command:

```bash
huggingface-cli delete-revisions <revision-id-1> <revision-id-2>
```

Replace `<revision-id-1>` and `<revision-id-2>` with the actual revision IDs you want to delete. You can find these IDs from the scan report you generated in Step 2.

## Step 4: Verifying Cache Clean-Up

After cleaning, you can run the scan command again to make sure your cache size has decreased:

```bash
huggingface-cli scan-cache
```

## Additional Tips

- Always double-check the revision IDs before deleting to avoid removing necessary data.
- Regular cache maintenance can help in managing disk space more effectively.

That's it! With these simple steps, you can keep your Hugging Face cache lean and efficient. For more detailed information and advanced options, be sure to check out the [Hugging Face CLI Guide](https://huggingface.co/docs/huggingface_hub/main/en/guides/cli).
