## v0.19.0
- \[enhancement\] use new getAuthenticationChallenge endpoint
- \[new feature\] send language header to Beard
- \[new feature\] new api for readings in history
- \[new feature\] ability to allowDownload when encrypting files or setting it later
- \[new feature\] lastNotifiedId read during searchEvents to skip events when already notified on another device
- \[new feature\] invitedBy in getTeamInvitations
- \[new feature\] added lastUpdated for users
- \[new feature\] eventDate read during searchEvents to skip updating the user if it is already updated after the eventDate
- \[new feature\] added docker files so we can run tests on it
- \[new feature\] handle events in a pagination of 100 event each time
- \[new feature\] childTree read during search events to see if the user is the owner and/or the forwarder
- \[new feature\] full database update when 1000 event have been missed


## v0.18.1
- \[new feature\] add revoked date in ACLs
- \[bugfix\] cleaner closing of file streams
- \[bugfix\] error management details
- \[removing deprecated\] removing invitations


## v0.18.0
- \[new feature\] licences & team management
- \[new feature\] message history
- \[new feature\] add reading information in ACLs
- \[new feature\] generate localized hairless files (i18n)
- \[new feature\] option to disable API waterfall
- \[enhancement\] switching everything crypto-related to SSCrypto
- \[enhancement\] new device now skips previous events and performs full DB update
- \[enhancement\] exporting a few functions useful for goatee-cli
- \[bugfix\] unsealStream now correctly returns UNKNOWN_PROTOCOL error on non-seald file
- \[bugfix\] fix error in login-log when there are failed logins (for exemple with revoked device) 
- \[bugfix\] fix a few race-conditions in account module


## v0.17.0

- \[new feature\] ACL module
- \[bugfix\] fix uncatchable errors when permission problems
- \[bugfix\] fix crossbar reconnection when first connection fails

## v0.16.1

- \[new feature\] add loginHistory
- \[bugfix\] fix race condition between scanning and promise for device-pairing-pin

## v0.16.0

- \[**breaking change**\] change `goatee.files` signatures (returning `messageId` on sealing)
- \[bugfix\] fix emailsToUIDs for default user & add emailsToRecipients (for goatee-local-server)
- \[bugfix\] fix iteration of missingMessageKeys pagination
- \[new feature\] allow override of massReencrypt (to be able to put it in thread/worker/...)
- \[new feature\] add a new optional initialisation argument `hairlessURL` for the url in hairless files
- \[bugfix\] fix cookie handling when fetch implementation concatenates multiple set-cookie headers
- \[new feature\] add an api point to get file messageId & key

## v0.15.0

- \[new feature\] Sending 'close' event on closing, possibly with error (`goatee.evenBus.on('closing', error => {})` / `goatee.evenBus.on('closed', () => {})`)
- \[new feature\] Closing with error on login fail
- \[**breaking change**\] Change signature of multidevice functions in `goatee.account` : now returning local `eventBus` and using it instead of `goatee.eventBus`
- \[bugfix\] now clearing multidevice timeout on error
- \[new feature\] `goatee.account.renameDevice`
- \[new feature\] check if API responses are indeed by beard
- \[bugfix\] on `goatee.files.unseal` no more temp filename collision
- \[new feature\] add connector state RM + no more useless follow
- \[new feature\] sync contacts between devices
- \[new feature\] `message-read` & `message-read-entrusted` events on `goatee.eventBus` when message is read for the first time
- \[**breaking change**\] change `goatee.files` signatures (ability to force `messageId` & `messageKey` on sealing / returning them on unsealing)
- \[bugfix\] fix invalid chars on `randomString`
- \[bugfix\] follow/unfollow event handlers will not trigger follow/unfollow api calls anymore
- \[bugfix\] fix `UIDsToKeys` : no more trying to encrypt for revoked keys

## v0.14.0

Start of changelog
