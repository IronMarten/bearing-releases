# bearing-releases

Releases for Bearing Pro, from Iron Marten. Each release is under
[Releases](https://github.com/IronMarten/bearing-releases/releases); the product page is
<https://ironmarten.com/bearing-pro/>.

## Verifying a download

Each release ships a `SHA256SUMS` file signed with the release key, `release.pub.asc` in this
repository. Before trusting the key, check its fingerprint against the one published on
<https://ironmarten.com/security/>:

```
A109 6721 7B42 D606 DCA6  726C 09A0 77AB B48A D4AE
Bearing release signing <chris@ironmarten.com> · Ed25519 · expires 2028-09-30
```

```
gpg --import release.pub.asc
gpg --fingerprint "Bearing release signing"
gpg --verify SHA256SUMS.asc SHA256SUMS
sha256sum -c SHA256SUMS
```

This key signs releases only. It is not the key that signs licences.
