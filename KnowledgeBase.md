## Know-how

### UI/UX
1. [Figma's Design Basics Articles](https://www.figma.com/resource-library/difference-between-ui-and-ux/)
2. [What is Wireframing? Explained by a Designer](https://weareripple.ca/wireframing-explained-by-a-designer/)
3. [Begineer's guide to Penpot UI design software](https://penpot.app/blog/penpot-ui-design-software-a-beginners-guide/)
4. [React Native Tutorial](https://reactnative.dev/docs/tutorial)

### Local Database
> NOTE: Should be offline-first and [CRDT-ready](https://crdt.tech/)
1. [RxDB](https://github.com/pubkey/rxdb)
2. [automerge](https://github.com/automerge/automerge)
3. [Some other CRDT implementations](https://crdt.tech/implementations)

### P2P communication
#### Local/Direct P2P
1. [React Native Multipeer Connectivity for iOS (uses Apple’s Multipeer framework)](https://github.com/react-native-webrtc/react-native-webrtc)
2. [Nearby Connections API for Android](https://developers.google.com/nearby/connections/overview)

#### WebRTC-based P2P
1. [React Native WebRTC Library](https://github.com/react-native-webrtc/react-native-webrtc)
2. [coturn](https://github.com/coturn/coturn) is an open-source TURN server you can self-host
3. TODO: look into how Brave, Signal use WebRTC for local-first, P2P communication

## Precedents
This model is inspired by existing local-first or P2P mobile apps:

| **App / Project** | **Approach**                | **Notes**                                                   |
|-------------------|-----------------------------|-------------------------------------------------------------|
| Manyverse (Scuttlebutt) | P2P social network          | Full offline sync, works over Bluetooth, Wi-Fi, Internet     |
| Briar             | Encrypted P2P messenger      | Android app using Bluetooth, Wi-Fi, Tor relays              |
| Syncthing         | P2P file sync               | Uses discovery servers + relays for mobile sync             |
| Delta Chat        | Email-based messenger       | Uses existing infrastructure, but local-first mindset       |
| Peergos           | P2P storage & sharing       | Uses WebRTC + self-hosted relays                            |


## Our core principles of design
1. Flexibility: Since this will be our first end-to-end product, we may have to move things around as we progress. Always take flexibility into consideration while designing/coding a feature: how much of an effort is it to add/modify a portion of this feature? 
2. Isolation: Expose relevant APIs strictly based on need.
3. Security: An app is only as safe as its weakest link. For every feature you develop, ask yourself this: what are all the ways this feature can malfunction? how do we prevent that?
4. Modularity: Split your end-to-end design into appropriate modules so that each can be developed simultaneoulsy. Lay out feature testing requirements each module must meet before we move onto integration testing.
5. Scalability: Every module and every feature should be easy to scale.
