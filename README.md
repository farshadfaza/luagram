# luagram - 1.0
 Lua telegram client

# [Telegram Group](https://t.me/luagramgroup)

# installing : lua >= 5.3

luarocks install luagram-client

## Using : 
- Import `luagram-client` into the bot.
- Call the functions.

See example script below.


```lua

local luagram = require 'luagram-client'
local app = luagram.set_config{
  api_id = 1234567,
  session_name = 'session_name',
  api_hash = 'api_hash',
  -- token = ''
}
function main(msg)
  if msg.content.text then
    if msg.content.text.text == 'ping' then
      app.sendText(msg.chat_id, msg.id, '<b> pong </b>', 'html')
    end
  end
end
luagram.run(main)


```
for get result  

```lua 
result = app.func ()
app.vardump(result)
```



## The Functions - version 1.0 Beta
- ```help(function_name or '*')```
- downloadFile(file_id, priority)
- ```readAllChatMentions(chat_id)```
- upgradeBasicGroupChatToSupergroupChat(chat_id)
- ```joinChatByInviteLink(invite_link)```
- getRecoveryEmailAddress(password)
- ```openChat(chat_id)```
- uploadFile(file, file_type, priority)
- ```getFileExtension(mime_type)```
- setChatDraftMessage(chat_id, reply_to_message_id, text, parse_mode, disable_web_page_preview, clear_draft)
- ```getChatEventLog(chat_id, query, from_event_id, limit, filters, user_ids)```
- add_events(def)
- ```removeFavoriteSticker(sticker)```
- setRecoveryEmailAddress(password, new_recovery_email_address)
- ```unblockUser(user_id)```
- addRecentSticker(is_attached, sticker)
- ```getSavedOrderInfo()```
- getChatHistory(chat_id, from_message_id, offset, limit, only_local)
- ```removeTopChat(category, chat_id)```
- getSupergroupFullInfo(supergroup_id)
- ```setSupergroupDescription(supergroup_id, description)```
- searchMessages(query, offset_date, offset_chat_id, offset_message_id, limit)
- ```checkChatUsername(chat_id, username)```
- createNewSecretChat(user_id)
- ```sendVideoNote(chat_id, reply_to_message_id, video_note, duration, length, thumbnail, thumb_width, thumb_height, disable_notification, from_background, reply_markup)```
- searchContacts(query, limit)
- ```createTemporaryPassword(password, valid_for)```
- getTemporaryPasswordState()
- ```getFileMimeType(file_name)```
- deleteProfilePhoto(profile_photo_id)
- ```searchStickerSets(query)```
- createSupergroupChat(supergroup_id, force)
- ```createPrivateChat(user_id, force)```
- getSupergroupMembers(supergroup_id, filter, query, offset, limit)
- ```setSupergroupStickerSet(supergroup_id, sticker_set_id)```
- reorderInstalledStickerSets(is_masks, sticker_set_ids)
- ```sendPhoto(chat_id, reply_to_message_id, photo, caption, parse_mode, added_sticker_file_ids, width, height, ttl, thumbnail, thumb_width, thumb_height, disable_notification, from_background, reply_markup)```
- getRecentStickers(is_attached)
- ```getChatMember(chat_id, user_id)```
- deleteSavedOrderInfo()
- ```closeChat(chat_id)```
- getRepliedMessage(chat_id, message_id)
- ```reportSupergroupSpam(supergroup_id, user_id, message_ids)```
- terminateSession(session_id)
- ```getChatReportSpamState(chat_id)```
- getPasswordState()
- ```getWebPagePreview(text)```
- addRecentlyFoundChat(chat_id)
- ```cancel_timer(timer_id)getMe()```
- getBasicGroup(basic_group_id)
- ```getCreatedPublicChats()```
- searchInstalledStickerSets(is_masks, query, limit)
- ```createNewSupergroupChat(title, is_channel, description)```
- setChatClientData(chat_id, client_data)
- ```removeSavedAnimation(animation)```
- exists(file_path)
- ```setPinnedChats(chat_ids)```
- getCallbackQueryAnswer(chat_id, message_id, payload, data, game_short_name)
- ```createCall(user_id, udp_p2p, udp_reflector, min_layer, max_layer)```
- getGroupsInCommon(user_id, offset_chat_id, limit)
- ```getBasicGroupFullInfo(basic_group_id)```
- searchPublicChats(query)
- ```sendChatSetTtlMessage(chat_id, ttl)```
- searchChatMembers(chat_id, query, limit)
- ```logOut()```
- getPublicMessageLink(chat_id, message_id, for_album)
- ```unpinSupergroupMessage(supergroup_id)```
- resetNetworkStatistics()
- ```sendInvoice(chat_id, reply_to_message_id, invoice, title, description, photo_url, photo_size, photo_width, photo_height, payload, provider_token, provider_data, start_parameter, disable_notification, from_background, reply_markup)```
- sendContact(chat_id, reply_to_message_id, phone_number, first_name, last_name, user_id, disable_notification, from_background, reply_markup)
- ```optimizeStorage(size, ttl, count, immunity_delay, file_type, chat_ids, exclude_chat_ids, chat_limit)```
- getChatPinnedMessage(chat_id)
- ```sendVideo(chat_id, reply_to_message_id, video, caption, parse_mode, added_sticker_file_ids, duration, width, height, ttl, thumbnail, thumb_width, thumb_height, disable_notification, from_background, reply_markup)```
- editMessageText(chat_id, message_id, text, parse_mode, disable_web_page_preview, clear_draft, reply_markup)
- ```vardump(input)```
- terminateAllOtherSessions()
- ```addNetworkStatistics(entry, file_type, network_type, sent_bytes, received_bytes, duration)```
- setNotificationSettings(scope, chat_id, mute_for, sound, show_preview)
- ```searchChatsOnServer(query, limit)```
- sendLocation(chat_id, reply_to_message_id, latitude, longitude, disable_notification, from_background, reply_markup)
- ```deleteChatMessagesFromUser(chat_id, user_id)```
- sendChatScreenshotTakenNotification(chat_id)
- ```reportChat(chat_id, reason, text, message_ids)```
- getRemoteFile(remote_file_id, file_type)
- ```createSecretChat(secret_chat_id)```
- sendSticker(chat_id, reply_to_message_id, sticker, width, height, disable_notification, thumbnail, thumb_width, thumb_height, from_background, reply_markup)
- ```sendDocument(chat_id, reply_to_message_id, document, caption, parse_mode, thumbnail, thumb_width, thumb_height, disable_notification, from_background, reply_markup)```
- sendAudio(chat_id, reply_to_message_id, audio, caption, parse_mode, duration, title, performer, thumbnail, thumb_width, thumb_height, disable_notification, from_background, reply_markup)
- ```sendAnimation(chat_id, reply_to_message_id, animation, caption, parse_mode, duration, width, height, thumbnail, thumb_width, thumb_height, disable_notification, from_background, reply_markup)```
- sendText(chat_id, reply_to_message_id, text, parse_mode, disable_web_page_preview, clear_draft, disable_notification, from_background, reply_markup)
- ```getTermsOfService()```
- getInviteText()
- ```setAccountTtl(ttl)```
- cancelUploadFile(file_id)
- ```deleteChatReplyMarkup(chat_id, message_id)```
- toggleChatIsPinned(chat_id, is_pinned)
- ```sendInlineQueryResultMessage(chat_id, reply_to_message_id, disable_notification, from_background, query_id, result_id)```
- createBasicGroupChat(basic_group_id, force)
- ```getFile(file_id)```
- deleteMessages(chat_id, message_ids, revoke)
- ```sendVoiceNote(chat_id, reply_to_message_id, voice_note, caption, parse_mode, duration, waveform, disable_notification, from_background, reply_markup)```
- getSecretChat(secret_chat_id)
- ```getChatMessageByDate(chat_id, date)```
- resetAllNotificationSettings()
- ```getSupportUser()```
- setNetworkType(type)
- ```clearImportedContacts()```
- setUsername(username)
- ```viewMessages(chat_id, message_ids, force_read)```
- getInlineQueryResults(bot_user_id, chat_id, latitude, longitude, query, offset)
- ```sendVenue(chat_id, reply_to_message_id, latitude, longitude, title, address, provider, id, disable_notification, from_background, reply_markup)```
- getStorageStatisticsFast()
- ```setUserPrivacySettingRules(setting, rules, allowed_user_ids, restricted_user_ids)```
- searchSecretMessages(chat_id, query, from_search_id, limit, filter)
- ```getStorageStatistics(chat_limit)```
- searchChats(query, limit)
- ```getArchivedStickerSets(is_masks, offset_sticker_set_id, limit)```
- getAccountTtl()
- ```getCountryCode()```
- getUser(user_id)
- ```setOption(name, option_value, value)```
- getOption(name)
- ```toggleSupergroupIsAllHistoryAvailable(supergroup_id, is_all_history_available)```
- getUserPrivacySettingRules(setting)
- ```importContacts(phone_number, first_name, last_name, user_id)```
- getWallpapers()
- ```getTrendingStickerSets()```
- getNetworkStatistics(only_current)
- ```deleteSavedCredentials()```
- closeSecretChat(secret_chat_id)
- ```deleteSupergroup(supergroup_id)```
- sendForwarded(chat_id, reply_to_message_id, from_chat_id, message_id, in_game_share, disable_notification, from_background, reply_markup)
- ```getChatAdministrators(chat_id)```
- getSavedAnimations()
- ```pinSupergroupMessage(supergroup_id, message_id, disable_notification)```
- getChats(offset_chat_id, limit, offset_order)
- ```searchStickerSet(name)```
- setPassword(old_password, new_password, new_hint, set_recovery_email_address, new_recovery_email_address)
- ```toggleSupergroupInvites(supergroup_id, anyone_can_invite)```
- setSupergroupUsername(supergroup_id, username)
- ```deleteChatHistory(chat_id, remove_from_chat_list)```
- toggleBasicGroupAdministrators(basic_group_id, everyone_is_administrator)
- ```getActiveSessions()```
- setBio(bio)
- ```setName(first_name, last_name)```
- set_timer(seconds, def, argv)
- ```get_timer(timer_id)```
- cancel_timer(timer_id)
- ```setProfilePhoto(photo)```
- removeRecentlyFoundChat(chat_id)
- ```sendMessageAlbum(chat_id, reply_to_message_id, input_message_contents, disable_notification, from_background)```
- searchPublicChat(username)
- ```recoverPassword(recovery_code)```
- clearRecentStickers(is_attached)
- ```setChatMemberStatus(chat_id, user_id, status, right)```
- getWebPageInstantView(url, force_full)
- ```removeRecentHashtag(hashtag)```
- searchHashtags(prefix, limit)
- ```getTextEntities(text)```
- addSavedAnimation(animation)
- ```getStickerEmojis(sticker)```
- getSupergroup(supergroup_id)
- ```searchStickers(emoji, limit)```
- getFavoriteStickers()
- ```blockUser(user_id)```
- viewTrendingStickerSets(sticker_set_ids)
- ```changeStickerSet(set_id, is_installed, is_archived)```
- createNewBasicGroupChat(user_ids, title)
- ```requestPasswordRecovery()```
- setChatPhoto(chat_id, photo)
- ```getChat(chat_id)```
- toggleSupergroupSignMessages(supergroup_id, sign_messages)
- ```getStickerSet(set_id)```
- forwardMessages(chat_id, from_chat_id, message_ids, disable_notification, from_background, as_album)
- ```getAttachedStickerSets(file_id)```
- deleteAccount(reason)
- ```getImportedContactCount()```
- searchCallMessages(from_message_id, limit, only_missed)
- ```addFavoriteSticker(sticker)```
- getStickers(emoji, limit)
- ```getUserProfilePhotos(user_id, offset, limit)```
- changeImportedContacts(phone_number, first_name, last_name, user_id)
- ```getUserFullInfo(user_id)```
- clearRecentlyFoundChats()
- ```setChatTitle(chat_id, title)```
- removeContacts(user_ids)
- ```sendChatAction(chat_id, action, progress)```
- getMessage(chat_id, message_id)
- ```getBlockedUsers(offset, limit)```
- generateChatInviteLink(chat_id)
- ```checkChatInviteLink(invite_link)```
- acceptCall(call_id, udp_p2p, udp_reflector, min_layer, max_layer)
- ```deleteFile(file_id)```
- getTopChats(category, limit)
- ```cancelDownloadFile(file_id, only_if_pending)```
- addChatMembers(chat_id, user_ids)
- ```addChatMember(chat_id, user_id, forward_limit)```
- openMessageContent(chat_id, message_id)
- ```getRecentInlineBots()```
- editMessageCaption(chat_id, message_id, caption, parse_mode, reply_markup)
- ```sendBotStartMessage(bot_user_id, chat_id, parameter)```
- getNotificationSettings(scope, chat_id)
- ```searchChatMessages(chat_id, query, filter, sender_user_id, from_message_id, offset, limit)```
- getMessages(chat_id, message_ids)
