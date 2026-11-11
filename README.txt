CLIP FACTORY — PRIVATE FRONT-END PREVIEW

WHAT WORKS IN THIS BUILD
- Responsive dashboard for phone and PC
- Streamer list for Twitch, YouTube and Kick
- Favorite streamer toggle and channel links
- Manual video upload into a local approval queue
- Approve/reject controls (approval does not publish)
- Browser-local persistence; uploaded video blobs are stored in IndexedDB
- Installable PWA shell when hosted over HTTPS

IMPORTANT LIMITS
This is the front-end preview, not the 24/7 production service. It does NOT yet:
- Monitor Twitch, YouTube or Kick streams in the cloud
- Automatically detect moments or create AI clips
- Sync your account, streamers or videos between phone and PC
- Send reliable push notifications while the browser is closed
- Publish to TikTok, YouTube Shorts or Instagram

Those require a secure backend and cloud worker, database/object storage, queue,
AI/video-processing pipeline, platform authorization/API integrations, and push
notification service. The approval gate must remain server-enforced so no clip can
publish without your explicit approval. Only process creator content you are
authorized to clip and republish, and follow each platform's terms.

RUN LOCALLY
Open index.html in a modern browser. For PWA/service-worker behavior, serve this
folder over HTTPS or localhost (for example, use a local static server).

DEPLOY FRONT END
Upload the contents of this folder to a static HTTPS host. This only publishes the
interface; it does not activate 24/7 stream monitoring. Do not put API keys or
passwords in this folder or browser code.

NEXT PRODUCTION BUILD
1. Private sign-in and server-side account/session management.
2. Database for creators, favorites, clips, approvals and publishing history.
3. Cloud worker that checks authorized creator live status continuously and queues
   recording/processing jobs according to platform permissions and API terms.
4. Video storage and AI highlight detection, transcription, captions and reframing.
5. Push notifications when a clip is ready.
6. Server-side approval endpoint; publishing workers accept only approved clip IDs.
7. OAuth publishing integrations where supported by each destination.
