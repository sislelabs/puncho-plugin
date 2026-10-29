# The static formats

Nine formats, each typed as `adFormat`. Top food and CPG accounts run six to
eight at once; variety across formats beats volume of one. Each entry: what it
proves, when to choose it, how it is built with this pipeline's tools, and what
ruins it.

## HEADLINE_PRODUCT — one line, the product as hero

- **Proves:** one specific claim, said with confidence, and what the product is.
- **Choose when:** the hook is strong alone and the pack is good-looking.
- **Build:** field in the pack's signature colour (or two planes, signature and
  paper). Headline huge, top third, paper or ink. Pack front-on, centre or
  lower third, `integrate_image` for a contact shadow. Optionally contents
  spilled at its foot (generated, cut out, `integrate_image`). Under the
  headline, a second level: the product's name and its one reason, and two or
  three short facts or a price sticker, set on the field or a carrier. In a
  scene (`IN_SCENE`), the product is big: half the frame's width or more, no
  wall of nothing between it and the headline.
- **Ruins it:** a second claim competing with the first; the pack small; the
  headline alone over an empty field, which says nothing to a stranger.

## CALLOUTS — the product with facts pointing at it

- **Proves:** what is in it, checkably. Reads as information, not promotion.
- **Choose when:** the product has 3–5 concrete facts buyers ask about
  (ingredient, origin, weight, what it lacks).
- **Build:** pack centre on its colour field. Each fact: a short number or word
  big, a two-word label small, an `icon` arrow (`arrow-curved` or `arrow-loop`,
  turned to aim) from the fact to the part of the pack it is about. Headline top,
  short. This is the batch's one ad with devices; no other ad in the batch
  uses arrows or rings.
- **Ruins it:** more than five callouts; arrows all the same angle; facts the
  label does not support.

## US_VS_THEM — ours against the default

- **Proves:** why this one, by contrast with what the reader buys now.
- **Choose when:** there is a checkable difference (butter vs vegetable fat,
  five ingredients vs a list).
- **Build:** two columns or a table with heavy rules. Ours: the real pack, warm
  material or the signature colour. Theirs: a blank generic pack (generated,
  unbranded, cut out) labelled "обикновени …" — a category, never a named
  rival. Rows of short lines with a full stop; `tick` and `cross` icons. Make the
  last row the punchline, a joke instead of a fact.
- **Ruins it:** naming a competitor; claims about them you cannot prove; rows
  that are adjectives.

## INGREDIENT_EXPLOSION — what is inside, flying out

- **Proves:** real ingredients, with motion and appetite on a still image.
- **Choose when:** the ingredients are visual (nuts, cocoa, berries, herbs).
- **Build:** pack centre, front-on or slightly turned, on a plain ground from its
  colours. Generate the ingredients flying outward from a clear centre, same
  light as the pack's shot, with the centre empty, then add several cut-out
  pieces as separate parts in front of the pack, at different sizes and with
  slight blur, for depth. Headline top. `add_grain` last.
- **Ruins it:** ingredients the product does not contain; a cluttered frame
  with no clear centre.

## STICKY_NOTE — words written by a person, stuck in a real moment

- **Proves:** a human truth, said like a note at home. Low polish reads as
  real and gets past the reader's ad filter.
- **Choose when:** the hook sounds like something a person would write on a
  note: a warning, a reminder, an instruction to a housemate.
- **Build:** a generated scene in natural light (a kitchen counter, a bowl, a
  fridge door, a gift bag) with the food in it and the note's spot visible.
  Generate the blank note as its own part (cut out, same light), place it on the
  object, turn and slant it to sit on the surface, and set the words on it in
  the handwriting face. A crumb or a piece of the food in the foreground, as
  another cut-out part, adds depth. Pack:
  `CORNER_PACK` small, or `NO_PACK` with the food recognisable.
  When the note is stuck on the product itself (`IN_SCENE`): place the real
  product, generate the blank note (cut out, flat, straight on) and lay it on
  the product's face, then `build_scene` with both in `layerIds`, so the
  photograph is made round the product with the note already on it. Set the
  words on the note after.
- **Ruins it:** typed-looking words on the note; a note floating off the
  surface; a polished studio scene.

## FOOD_IN_HAND — appetite in motion, the pack in the corner

- **Proves:** that it is irresistible, by showing someone unable to resist.
- **Choose when:** the hook is an exclamation or a confession.
- **Build:** a generated photograph as the hero: a hand reaching into a bowl or
  lifting a spoon, the food close, two-plane background (wall and surface) in
  the pack's colours, side light, the top third clean wall for the headline.
  Add foreground food (a crumb, a drip, a piece mid-fall) as cut-out parts in
  the same light. The real pack flat in a lower corner (`CORNER_PACK`), soft
  drop shadow. Headline huge, chunky, top-left, the hand reaching into it if
  possible.
- **Ruins it:** the hand's anatomy (check the fingers); the pack too big; the
  headline on the busy part of the photo.

## DATA_HERO — one number

- **Proves:** a single fact so specific it is persuasive by itself.
- **Choose when:** there is one striking, true number (one ingredient, 3
  spoons, 0 added sugar, 250 g of only nuts).
- **Build:** the number enormous (a quarter of the frame or more), what it
  means in one small line under it, pack beside it. Flat field from the pack.
  Nothing else.
- **Ruins it:** two numbers; a number that needs an asterisk.

## PERSON_NOTE — someone's own words

- **Proves:** trust, through a real person's voice (a founder, a customer).
- **Choose when:** there is a real quote with a surprising specific, or a
  founder's line only they could say. Never invented.
- **Build:** the words large, as a handwritten note, a card or a plain quote with
  the name small under it; a real photo of the person or their hands with the
  product; stars as `star` icons only for a real review.
- **Ruins it:** generic praise; an invented customer; a stock face.

## NATIVE_SCREEN — a chat, a note, a notification

- **Proves:** a relatable moment in the reader's own interface; reads as
  content, not as an ad.
- **Choose when:** the hook is dialogue, a list someone would keep, or a
  message someone would get.
- **Build:** the screen as the whole picture (full-bleed, the platform's own
  look: real bubble shapes, real spacing, system font sizes) or a phone held in
  a real moment with the screen as a separate layer. The product appears in the
  conversation itself (a photo sent in the chat) or as the real moment behind.
  Never a mock-up floating on white above a separate photo.
- **Ruins it:** a fake-looking interface; a fabricated post presented as real;
  words laid outside the screen, such as a footer of dates, an address or a
  URL printed on the scene round the phone. What the screen does not say goes
  in the primary text.
