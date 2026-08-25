# L-DCA Codebook — FLP course evaluation comments (10 codes, multi-label)

Each comment receives ZERO OR MORE of the following 10 codes (a comment may carry
several). Apply a code only if the comment's text gives explicit support for it.
The comments are in Colombian Spanish; preserve meaning, do not over-infer.

1. METpos — Praises the inverted/flipped METHODOLOGY or class structure itself
   (e.g., flipped helps, "optimiza el tiempo", clase más dinámica/práctica gracias
   al método, resolver dudas en clase). About the teaching MODEL, not the person.
2. METneg — Criticizes or REJECTS the flipped methodology / class model itself
   (e.g., "el modelo no funciona", clase pasiva por el método, the inverted format
   is bad). About the MODEL, not difficulty in general.
3. VIDpos — Praises the PRE-CLASS VIDEOS or recorded material specifically.
4. VIDneg — Complains about the VIDEOS: too many, overload, too long, tedious
   ("ver 15 videos", "tortura").
5. ENGpos — Reports improved COMPREHENSION / learning / understanding / engagement
   ("entendí mejor", "aprendí", "pude practicar").
6. ENGneg — Complains about DIFFICULTY / PACE / workload of the course: too hard,
   too fast, "no se le puede seguir el ritmo", materia muy pesada/compleja.
7. MOTpos — Praises the INSTRUCTOR personally: enthusiasm, dedication, clarity,
   willingness to help, good attitude ("el profe es genial", "muy claro").
8. MOTneg — Concern about the INSTRUCTOR: loss of vocation, disengagement,
   demotivation, bad attitude, "perdida en la vocacion", not caring.
9. SPA — Mentions PHYSICAL classroom conditions: room, heat/calor, "sala de
   sistemas", salón, infrastructure, lack of computers.
10. AI — References GENERATIVE AI / ChatGPT / "inteligencia artificial" / IA tools.

Additionally assign one overall VALENCE for each comment:
- "positive": the comment is on balance favorable.
- "negative": the comment is on balance unfavorable/critical.
- "mixed": clearly both praise and criticism, or neutral/ambiguous.

Output rules: codes use EXACTLY these tokens: METpos METneg VIDpos VIDneg ENGpos
ENGneg MOTpos MOTneg SPA AI. If a comment supports none, use an empty code list.
