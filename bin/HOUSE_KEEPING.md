# HOUSE_KEEPING

## Cleanup dead links

TODO

## Fetching RSS Feeds

Use `bin/fetch_rss` to automatically discover and update RSS feeds:

```bash
# Update only unlocked entries (default)
bin/fetch_rss data/personal.yml

# Force update all entries in a category
bin/fetch_rss --force all data/newsletter.yml

# Update only entries without RSS feeds
bin/fetch_rss --force norss data/company.yml data/personal.yml
```

Available force modes:
- `unlocked` (default): Only update unlocked entries. Allows fine grained search on specific blog entries.
- `all`: Update all entries regardless of lock status
- `norss`: Update only entries that don't have RSS feeds

**Note:** Web archive entries are never updated regardless of the mode or lock status.