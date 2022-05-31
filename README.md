Includes mongodb dumps in /bson, and JSON formatted exports in /json.

The collections are all zipped and split into 50MiB chunks (minus the metadata) to make GitHub happy.

Collections that handled account configuration, sessions, and website configuration are not included.

# January 2021 PP changes

The `old_pp` of scores were meant to hold the historical PP of a score prior to the January 2021 PP changes, as a last-minute solution to handle snapshots. Due to an oversight all top 100 performances which were fetched by osu!stats around January 16-17 2021 won't have their old PP stored as intended. It will be the new PP value instead.

As a result, you can't reliably use `old_pp` with snapshots from January 17 2021 and prior, as many scores won't have the correct PP stored in `old_pp`. To resolve this you would have to iterate over scores which were updated after January 15 and re-calculate their old_pp value using the old calculations.
