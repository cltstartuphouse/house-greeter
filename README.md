# house-greeter

An agent that welcomes people when they walk into CLT Startup House and helps them find their way around, built on the house's Arduinos.

The first version gets built by the room at House Jam Nº 6 on Thursday, November 5, 2026, at CLT Startup House in Charlotte. It's open source, and the house keeps using it after tonight.

## The problem

People walk in and don't know where to go, what's on tonight, where the coffee is or how to get on the wifi. A host can't be at the door all the time. The greeter can.

## Ideas to start from

| Idea | What that means |
| --- | --- |
| Say hello | Notice someone at the door and greet them |
| Answer the basics | Wifi, parking, where the coffee is, what's on tonight |
| Know the calendar | Pull today's events from the house's public calendar and point people to the right room |
| Watch a shelf | Stretch goal: a camera pointed only at a shelf that notices what's missing, for [house-inventory](https://github.com/cltstartuphouse/house-inventory) |

**Done for tonight** is the smallest thing that runs end to end: someone walks up, the greeter notices and says hello, and it can answer one question.

## Start here

1. Read [CONTRIBUTING.md](CONTRIBUTING.md). It has a no-terminal path if you've never used git.
2. Pick an issue labeled for your level and comment "I'm on this":
   - [`level: beginner`](https://github.com/cltstartuphouse/house-greeter/issues?q=is%3Aissue+is%3Aopen+label%3A%22level%3A+beginner%22): the FAQ, greeting lines and wiring docs
   - [`level: intermediate`](https://github.com/cltstartuphouse/house-greeter/issues?q=is%3Aissue+is%3Aopen+label%3A%22level%3A+intermediate%22): greeting, answers, calendar and push-to-talk
   - [`level: advanced`](https://github.com/cltstartuphouse/house-greeter/issues?q=is%3Aissue+is%3Aopen+label%3A%22level%3A+advanced%22): the board, the architecture and presence detection
3. Issue #1, "Pick the board and the architecture," merges first. Until it does, work on the FAQ and greeting lines or pair with that group.

## Hardware

The house has Arduinos you can build with tonight. They belong to the house: build with them here and leave them here. Issue #1 records the exact board and parts. Commit source code only, never compiled firmware.

## Privacy rules

The greeter sits at the front door of a place people trust, so these aren't optional:

- **No face recognition and no names.** It greets everyone the same way.
- **No recordings.** Don't save audio, video or images of people.
- **Push-to-talk only.** No always-on microphone.
- **The shelf camera points at the shelf.** It processes frames on the device and stores none.
- **Public calendar data only.** Event names and times from the house's public calendar. Never guest lists.
- **Private answers stay private.** The wifi password, door codes and anything else private go in `docs/faq.local.md` on the device, which git ignores. The repo only has [`docs/faq.example.md`](docs/faq.example.md) with placeholders.
- **No keys in code.** If you use an AI model, your key goes in a `.env` file, which git ignores.

## How changes land

Fork the repo, make your change on a branch and open a pull request into `main`. Automated checks run on every pull request, and a maintainer reviews and merges. See [CONTRIBUTING.md](CONTRIBUTING.md) and [SECURITY.md](SECURITY.md).

## License

[MIT](LICENSE). By contributing, you agree your work is licensed the same way.

Proximity creates collisions. Collisions create breakthroughs.
