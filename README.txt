PLAYZZONE-GOLD v3 — Combined Page 11.00 to 13.52
===================================================
A combined single-page interface from two pages with the same golden theme.
MERGE: GOLD (11.00-13.00) + NEW CHAIN (13.02-13.52)

===========================================================
 Usage
===========================================================
1) Upload the contents of this folder as-is to any static web host (e.g., GitHub Pages).
2) Open the site link on your PS4 browser.
3) Two option cards will appear:

   • Option 1 — [11.00 ← 13.00] : Golden Series (GoldHEN) —
     defaults to the poops chain, or the alternate lapse chain via
     index.html?bug=lapse.

   • Option 2 — [13.02 ← 13.52] : New Chain (663) —
     tailored for firmware 13.02 up to 13.52 (jb.html).

4) After selection: The page automatically downloads AppCache files
   with a golden progress bar and percentage — once completed, the exploit
   page opens directly. The first online visit downloads both chains, and
   afterwards, everything runs completely offline without internet, with
   the payload (GoldHEN / payload2.bin) stored inside the cache.

5) Auto-Detection: The page automatically detects your firmware version via
   User-Agent and highlights the appropriate card while allowing you the 
   freedom to choose manually.

6) Test Options:
   index.html?fw=13.00   Test the interface with a specific firmware without a console
   index.html?bug=lapse  Force the LAPSE chain inside Option 1
   jb.html?log=1         Full execution log for the new chain

===========================================================
 Files
===========================================================
Gold Series — Original without any modifications (matching v2.1):
  index.html (new v3 combined version) / run_poops.html /
  run_lapse.html / chain_poops.js / chain_lapse.js / core.js /
  mem.js / int64.js / ps4_offsets.js / rpc_worker.js /
  payload.bin (GoldHEN) / patches/*.bin / ko-files/ / logo_playzone.png

New Chain — Files renamed to avoid conflicts with the Gold series 
(all files in both chains have different contents):
  jb.html (new golden UI with jb.js bindings) / jb.js /
  jb_core.js / jb_mem.js / jb_int64.js / jb_offsets.js /
  jb_rpc_worker.js / payload2.bin / patches/1350.bin / patches/1352.bin
  (13.02 and 13.04 in the new chain use patches/1302.bin listed
  above — no additional file needed)

  Only two lines were modified in the new chain files — import
  paths in jb.js and jb_mem.js to point to jb_* names — no changes
  to any exploit logic or payloads.

Note: This version only builds for 13.02 up to 13.52 in the new chain
(13.02/13.04/13.50/13.52), and Gold series from 11.00 up to 13.00.
Original pre-modification backup: C:\temp\ps4_web_original

===========================================================
 Offline AppCache — v3
===========================================================
The cache.appcache file follows the proven v2.1 format (no # comments
inside link lines) and now includes both sides' chains:
  • GOLD pages: index / run_poops / run_lapse (with ?ui=3 for each)
  • GOLD files: chain_*.js?ui=3 , core.js & core.js?v=10 , mem.js ,
    int64.js , ps4_offsets.js , rpc_worker.js , payload.bin ,
    patches/1100..1304.bin , logo_playzone.png
  • NEW pages: jb.html and jb.html?log=1
  • NEW files: jb.js?v=10 , jb_core.js?jbv=10 , jb_mem.js ,
    jb_int64.js , jb_offsets.js , jb_rpc_worker.js , payload2.bin ,
    patches/1350.bin , patches/1352.bin
  • patches/1302.bin and 1304.bin added (missing in v2.1 cache)
NETWORK:* and FALLBACK:/ index.html remain as they were.

How to update later when modifying any file: Change the comment version 
at the top of the file (v3 → v4) or change the version number in the 
links (?v=10 → ?v=11) so every console re-downloads the cache on the 
next online visit — users do not need to clear cache manually.

===========================================================
PLAYZZONE-GOLD v3 — with love, play_zzone
