# Keys the Agent Needs

Add each key in **GitHub → Settings → Secrets and variables → Actions** using the exact name below. Never paste a real key into this file or any other file in the repo.

| Secret name | What it's for | Where to get it |
|---|---|---|
| `ANTHROPIC_API_KEY` | Claude, which runs every skill | console.anthropic.com → API Keys |
| `META_APP_ID` | Facebook and Instagram posting | developers.facebook.com → My Apps → your app |
| `META_APP_SECRET` | Facebook and Instagram posting | Same app → Settings → Basic |
| `META_PAGE_ACCESS_TOKEN` | Posting to the Facebook Page and its connected Instagram | Graph API Explorer → long-lived Page token |
| `FACEBOOK_PAGE_ID` | Which Facebook Page to post to | Page → About → Page transparency, or Graph API Explorer |
| `INSTAGRAM_BUSINESS_ACCOUNT_ID` | Which Instagram account to post to (must be a Business or Creator account linked to the Page) | Graph API Explorer → `me/accounts?fields=instagram_business_account` |
| `PINTEREST_ACCESS_TOKEN` | Pinterest posting | developers.pinterest.com → My apps |
| `PEXELS_API_KEY` | Free stock photos and footage | pexels.com/api |
| `GOOGLE_SERVICE_ACCOUNT_JSON` | Reading and saving files in the brand's Drive folders | Google Cloud Console → IAM → Service accounts → Keys (share the brand's Drive folders with the service account's email) |
| `MEDIA_STORAGE_KEY` | Uploading media to the public storage the platforms download from | Your storage provider |

## Plug-in slots (add when connected)
| Secret name | What it's for |
|---|---|
| `TIKTOK_ACCESS_TOKEN` | TikTok posting (needs TikTok's app review for direct posting) |
| `YOUTUBE_CLIENT_SECRET_JSON` | YouTube Shorts uploads |
| `LINKEDIN_ACCESS_TOKEN` | LinkedIn posting |
| `SCHEDULER_APP_KEY` | A scheduling app, if one is used instead of direct posting |
| `VIDEO_EDITOR_KEY` | The team's video editor, if it needs a key |
