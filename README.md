1. Create a sub directory named 'job' in your Jellyfin config directory

2. Copy the get-tvguide bash script into the job folder. Ensure the permissions and owner is correct.
   - Example: -rwxr--r-- 1 root root 3197 Nov  3 08:07 get-tvguide

3. Update the configuration parameters section with your values:
   - HDHomeRun IP Address
   - Jellyfin URL (Example: http://1932.1678.1.123:8096)
   - Jellyfin API Key (This can be generated in Jellyfin > Dashboard > API Keys)
   - Verify/update the Jellyfin base URL for JELLYFIN_CFG, TVSCRIPT_DIR, and TVSCRIPT_LOG

4. Use cron to schedule the script to run periodically
   - Example: 0 6,18 * * * /DATA/AppData/jellyfin/config/job/get-tvguide
   - (this will run the script at 6am and 6pm each day)
