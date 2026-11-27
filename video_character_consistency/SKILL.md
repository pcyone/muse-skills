# Video Character Consistency

## Lock one identity reference

- Pick one identity frame for each outfit and reuse that same frame for every clip in the series.

- Do not build a multi angle asset set, because extra references can be averaged or picked at random and make the face drift sooner.

- Tell the user plainly that there is no seed or face lock switch in Muse video, so a reference image is a strong hint and not a guarantee.

## Reuse one description block verbatim

- Write one fixed physical description block and paste it unchanged into every generation prompt.

- List every locked attribute from the brief in the block, such as hairband length, fan, embroidery, and age, so acceptance can tick each item.

- Do not rewrite the block for variety, because a fresh description is a fresh chance for the face to change.

## Generate from the identity frame

- Start from the identity frame as the first frame when image to video is available.

- Change only one variable per generation, such as pose or camera angle, and keep face, outfit, and scene fixed.

## Accept each locked attribute from a clean anchor

- Write the acceptance list from the brief before you check a rebuild, and tick face, age, robe, fan, hairband, and embroidery separately for each mirror.

- Do not pass a rebuild when you have checked only face and robe.

- Pick the reference frame for the next clip from a clean moment inside the clip, and write down its timestamp, such as the 2.0 second frame when the end frame is polluted.

- Do not chain a reference from a generated clip that already drifted, and restart from the identity frame instead.

- Name the item that failed and the timestamp where you saw it when you reject a candidate.

## Select by extracted frames and check seams

- Generate more than one candidate when the clip matters, then extract frames and compare concrete points such as eye spacing, nose to lip ratio, and hair parting.

- Check a multi clip sequence by splicing the last half second of one clip with the first half second of the next clip and playing that join slowly.

- State the ceiling honestly when drift remains, because perfect identity across many clips is not currently achievable.

## Available connectors

- Use muse.connector_search to find other connectors and muse.skill_search to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with Custom Connectors and MCPs, or build a custom connector.

## Alternatives for better results

- Shorten a clip or split a scene when a long clip drifts, and restart the next clip from the identity frame.

- Accept a close match with a visible selection note when a perfect match is unavailable, and name which points matched and which did not.
