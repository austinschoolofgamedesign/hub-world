# Player State as a Petri net

The idea here is to map out a couple of characters movement sets as different states.
Like Mario is idle, and then you press the jump button and he goes into a jump state.

What are the states Mario can get to from there?

Once his trajectory is downward, he can land on an enemie's head and not get hurt.
He can also adjust his direction a little bit while in the air.
And he can land on the ground and return to idle.

I think I want to map this via intent, not via buttons on the controller.
It would be tempting to say something like "Hold `B` while pressing `D-Pad Right` to enter the `Run` state."
But that would make it too concrete I think.
There's no telling what kind of controller they're using.
The game isn't looking for the `B` button, it's looking for the input code triggered by that physical button press.
So it makes most sense to me to use the intent of that button.

Referring to them as `Dash`, `Jump`, and `Right` makes most sense to me.

---

- Donkey Kong arcade game movement.
  - Mario NES movement
  - VS other Marios would be an interesting analysis
- Link (OoT) movement/combat
  - VS other Links would be an interesting analysis
- Gohma (OoT) boss states
  - This could be an interesting comparison of boss states for analysis