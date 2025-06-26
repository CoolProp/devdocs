### Make token for access to this repo:

1. Click “Generate new token” → “Fine-grained token”
2. Name the token and set an expiration (recommended).
2. Select the repository you want it to access (this repo).
3. Permissions:
  Under Repository Permissions:
    Actions → Read and Write
    Contents → Read-only (or Read & Write if needed)
4. Generate the token and copy it immediately (you won’t see it again).


### Make token for CoolProp main repo:

Same as above, but give access to CoolProp instead

### Test it:
```
curl -X POST https://api.github.com/repos/CoolProp/devdocs/dispatches \
  -H "Accept: application/vnd.github+json" \
  -H "Authorization: token github_pat_11AAOh" \
  -d '{"event_type":"triggered-by-CoolProp-main","client_payload":{"example":"data"}}'
```