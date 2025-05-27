# PhotonNetworkAsync

🚀 **PhotonNetworkAsync** is a complete rework of PhotonNetwork APIs but with **async/await** and zero `bool` nonsense!
It’s so clean and modern that even Steve—the clumsy coffee spiller and manager—can’t mess it up (though he probably still will, because he *never tests things*).

---

## ☕️ Meet Steve, the “Manager”

Steve always says:

> “Yeah, I *kinda* tested it… let’s push to production!”

This project is for developers who want to avoid Steve’s eternal loop of “didn’t test, let’s debug live,” and instead **embrace the sweet flow of `async/await`**.

---

## 🌟 Features Steve (probably) didn’t read:

✅ **Async/Await for everything!**
✅ **No bool returns** – you’ll get proper exceptions instead.
✅ **Wraps** Photon’s callbacks like OnConnectedToMaster, OnJoinedRoom, etc.
✅ **Cleaner code**: even Steve can’t spill coffee on it!

---

## 🤯 Why Bother?

Photon’s usual API feels like:

```csharp
bool connected = PhotonNetwork.ConnectUsingSettings();
if (!connected)
{
    // Sad face
}
```

Steve says, “Yeah, that’s cool, right?”
But you? You want **real error handling**:

```csharp
try
{
    await PhotonNetworkAsync.ConnectUsingSettingsAsync();
    await PhotonNetworkAsync.JoinOrCreateRoomAsync("Room42", new RoomOptions { MaxPlayers = 4 });
}
catch (Exception e)
{
    Debug.LogError($"Photon error (Steve definitely didn’t test this): {e.Message}");
}
```

---

## 🍵 What’s Included?

✅ `ConnectUsingSettingsAsync()`
✅ `ConnectToRegionAsync(region)`
✅ `CreateRoomAsync(roomName, options, lobby)`
✅ `JoinRoomAsync(roomName)`
✅ `JoinRandomRoomAsync()`
✅ `JoinOrCreateRoomAsync(roomName, options, lobby)`
✅ `JoinLobbyAsync(lobby)`
✅ `LeaveLobbyAsync()`
✅ `LeaveRoomAsync()`
✅ `DisconnectAsync()`
# & M O R E!

---

## 📦 How to Use

1. **Download** `PhotonNetworkAsync.cs`.
2. **Add** it to your Unity project’s scripts.
3. **Replace** Photon’s old-school calls with shiny new async calls.

   * Example:

     ```csharp
     await PhotonNetworkAsync.CreateRoomAsync("RoomWithSteve", new RoomOptions { MaxPlayers = 6 });
     ```
4. **Try/Catch everything**. Trust us—Steve *never tests things*.

---

## ⚠️ Steve’s Warning Board

> “I didn’t really read the docs, but it should work!”
> ✅ Steve’s testing coverage = zero.
> ✅ Our testing coverage = more than zero (not Steve-level).

---

## 🛠️ Contributing

Want to add more Photon APIs?
✅ Fork
✅ PR
✅ Let’s keep Steve away from the main branch!

---

## 🗂️ License

MIT. Because Steve didn’t read the license either.

---

## 🧃 Final Words

With **PhotonNetworkAsync**, even Steve can pretend to be a pro (until he spills coffee again).
✨ Enjoy your cleaner, more modern, and way less Steve-ified Photon workflows!

---

**P.S.** If you see Steve around… maybe take his coffee away. ☕️
