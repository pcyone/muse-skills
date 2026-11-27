# Douyin Poetry Subtitle and Corrected Render Check

## Count the hook speech segments before timing subtitles

- Transcribe the narration audio before you time any subtitle, and count the hook speech segments from the transcription rather than from the script.

- Treat each phrase separated by a pause as its own segment, and write the segment count down before you assign any subtitle timing.

- Compare the transcription segment count with the script segment count, and stop when the two counts differ until you find which phrase was split or merged.

- Assign one subtitle line to each poem line only after the hook segments are counted, so no poem line airs one sentence early.

- Give the final poem line a subtitle of its own, and leave a line without a subtitle only when the narration is silent at that moment.

## Verify every subtitle against the frames

- Check the rendered video frame by frame at each subtitle boundary before you publish it or hand it over.

- Confirm each poem line appears exactly while its narration sounds, and confirm no subtitle appears during silence before the line starts.

- Confirm the last poem line shows its subtitle while it is spoken, and confirm no subtitle is missing at the end.

- Check the second half of the video for poem and picture mismatch as well as the opening, and flag any gate plaque or scroll text that carries illegible generated characters.

- Hold the video from publishing when any line is early, late, or missing, and re-time it before you check again.

## Deliver a corrected render under a new filename

- Save every corrected render under a new filename, and never reuse the filename of the version it replaces.

- Re-verify the attachment you send is the new render by checking its timestamps and frames, and do not trust the filename alone.

- State the frame timestamps you checked when you deliver the corrected file, so the user can confirm the fix without asking again.

- Ask the user whether to delete and repost when a published cut is misaligned, because a corrected file does not retract the published version.

## Available connectors

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with the Muse guide to custom connectors and MCPs, or build a custom connector.

## Alternatives for better results

- Run the hand post copy scope check on the post copy before delivery, since a correct subtitle check does not prove the copy scope is correct.

- Re-check the earlier days in the same series when one day misaligns, because the same counting slip can hide in a video that looked clean.
