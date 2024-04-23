### 1. Application Schema (`application.js`)

**Purpose:** Manages application submissions for a Discord server.

**Fields:**
- `GuildId`: The ID of the Discord server.
- `SubmissionChannel`: The channel where submissions are made.
- `ReviewerRoles`: Roles that can review submissions.
- `MaxForms`: The maximum number of forms allowed.
- `Forms`: An array of forms, each containing:
 - `name`: The name of the form.
 - `questions`: An array of questions in the form.
 - `Submissions`: An array of submissions, each containing:
    - `UserId`: The ID of the user who submitted.
    - `SubmissionId`: The ID of the submission.
    - `MessageId`: The ID of the message containing the submission.
    - `Status`: The status of the submission.
    - `Reason`: The reason for the submission status.
    - `Answers`: Answers to the form questions.
    - `Reviewer`: The ID of the reviewer.

### 2. Ban Log Schema (`banlog.js`)

**Purpose:** Logs ban actions performed on users.

**Fields:**
- `messageId`: The ID of the message related to the ban.
- `userId`: The ID of the user who was banned.
- `username`: The username of the user who was banned.
- `reason`: The reason for the ban.
- `moderator`: The ID of the moderator who performed the ban.
- `timestamp`: The time the ban was performed.

### 3. Bolo Log Schema (`bololog.js`)

**Purpose:** Logs bolo (bulletin) actions performed on users.

**Fields:**
- `messageId`: The ID of the message related to the bolo.
- `userId`: The ID of the user who was the target of the bolo.
- `username`: The username of the user who was the target of the bolo.
- `reason`: The reason for the bolo.
- `moderator`: The ID of the moderator who performed the bolo.

### 4. Kick Log Schema (`kicklog.js`)

**Purpose:** Logs kick actions performed on users.

**Fields:**
- `messageId`: The ID of the message related to the kick.
- `userId`: The ID of the user who was kicked.
- `username`: The username of the user who was kicked.
- `reason`: The reason for the kick.
- `moderator`: The ID of the moderator who performed the kick.

### 5. Moderation Schema (`moderation.js`)

**Purpose:** Manages moderation actions and settings for a Discord server.

**Fields:**
- `GuildId`: The ID of the Discord server.
- `UserId`: The ID of the user being moderated.
- `actions`: An array of moderation actions, each containing:
 - `actionId`: The ID of the action.
 - `actionType`: The type of action.
 - `reason`: The reason for the action.
 - `moderatorId`: The ID of the moderator who performed the action.
 - `timestamp`: The time the action was performed.
- `settings`: Moderation settings for the server.

### 6. Roblox Schema (`roblox.js`)

**Purpose:** Manages Roblox-related punishments and roles for a Discord server.

**Fields:**
- `Guild`: The name of the Discord server.
- `GuildId`: The ID of the Discord server.
- `Channel`: The channel where Roblox-related actions are logged.
- `PRoles`: Roles that can perform Roblox-related actions.

### 7. Session Schema (`session.js`)

**Purpose:** Manages sessions for a Discord server.

**Fields:**
- `Guild`: The name of the Discord server.
- `GuildId`: The ID of the Discord server.
- `Channel`: The channel where sessions are managed.
- `Name`: The name of the session.
- `Owner`: The ID of the session owner.
- `Votes`: Votes related to the session.
- `Code`: The code for the session.
- `PRoles`: Roles that can participate in the session.
- `Ping`: The ping for the session.
- `VoteDM`: Whether to send vote DMs.

### 8. Shifts Schema (`shifts.js`)

**Purpose:** Manages staff shifts for a Discord server.

**Fields:**
- `Guild`: The name of the Discord server.
- `GuildId`: The ID of the Discord server.
- `UserId`: The ID of the user.
- `Username`: The username of the user.
- `ShiftActive`: Whether the user's shift is active.
- `Shifts`: A map of shifts, each containing:
 - `ShiftType`: The type of shift.
 - `StartTimestamp`: The start timestamp of the shift.
 - `EndTimestamp`: The end timestamp of the shift.
 - `Pauses`: A map of pauses within the shift.

### 9. Staff Schema (`staff.js`)

**Purpose:** Manages staff data for a Discord server.

**Fields:**
- `Guild`: The name of the Discord server.
- `GuildId`: The ID of the Discord server.
- `Promotions`: Promotions channel log.
- `Demotions`: Demotions channel log.
- `Strikes`: Strikes channel log.
- `LoAs`: Leaves of Absence channel log.
- `CanBypassAntiPing`: Whether staff can bypass anti-ping.
- `ReviewChannel`: The channel for reviews.
- `AntiPingRoles`: Roles that can bypass anti-ping.
- `PRoles`: Roles that can perform certain actions.
- `StaffRoles`: Staff roles.
- `StrikeRoles`: Strike roles.
- `HRRoles`: HR roles.
- `Cooldown`: A cooldown period.
- `Cooldowns`: An array of cooldowns.

### 10. Staff Members Schema (`staffMembers.js`)

**Purpose:** Manages individual staff member data for a Discord server.

**Fields:**
- `Guild`: The name of the Discord server.
- `GuildId`: The ID of the Discord server.
- `members`: A map of staff members, each containing:
 - `Promotions`: An array of promotions.
 - `Demotions`: An array of demotions.
 - `Strikes`: An array of strikes.
 - `TotalShiftDuration`: The total duration of shifts.
 - `OnDutyShiftDuration`: The duration of on-duty shifts.
 - `LoA`: A map of Leaves of Absence.
 - `RA`: A map of Requested Absences.

### 11. User Strikes Schema (`strikes.js`)

**Purpose:** Manages user strikes for a Discord server.

**Fields:**
- `_id`: The ID of the strike.
- `UserId`: The ID of the user who received the strike.
- `GuildId`: The ID of the Discord server.
- `Reason`: The reason for the strike.
- `Duration`: The duration of the strike.
- `EndTime`: The end time of the strike.

### 12. Themes Schema (`themes.js`)

**Purpose:** Manages themes for a Discord server.

**Fields:**
- `GuildId`: The ID of the Discord server.
- `PrimaryColor`: The primary color of the theme.
- `SecondaryColor`: The secondary color of the theme.
- `TertiaryColor`: The tertiary color of the theme.
- `Green`: A green color.
- `Red`: A red color.
- `LightBlue`: A light blue color.
- `DarkBlue`: A dark blue color.
- `White`: A white color.
- `Transparent`: A transparent color.
- `PrimaryImageUrl`: The URL of the primary image for the theme.

### 13. Ticket Analytics Schema (`ticketAnalytics.js.scrapped`)

**Purpose:** Manages ticket analytics for a Discord server.

**Fields:**
- `GuildId`: The ID of the Discord server.
- `TicketCategories`: An array of ticket categories.
- `SupportRoles`: An array of support roles.
- `TotalTicketsOpened`: The total number of tickets opened.
- `TotalTicketsClosed`: The total number of tickets closed.
- `TotalMessages`: The total number of messages.
- `CloseTimes`: An array of close times.
- `UserAnalytics`: An array of user analytics, each containing:
 - `UserId`: The ID of the user.
 - `TicketOpenedAt`: The time the ticket was opened.
 - `LastResponseAt`: The time of the last response.
 - `LastRequesterMessageAt`: The time of the last requester message.
 - `AvgInitialResponseTime`: The average initial response time.
 - `AvgResponseTime`: The average response time.
 - `AvgCloseTime`: The average close time.
 - `TotalResponses`: The total number of responses.
 - `TotalTickets`: The total number of tickets.
 - `TotalTicketsResolved`: The total number of resolved tickets.
 - `TotalTicketsEscalated`: The total number of escalated tickets.
 - `TotalTicketsReopened`: The total number of reopened tickets.

### 14. Warn Log Schema (`warnlog.js`) (Continued)

**Purpose:** Logs warn actions performed on users.

**Fields:**
- `messageId`: The ID of the message related to the warn.
- `userId`: The ID of the user who was warned.
- `username`: The username of the user who was warned.
- `reason`: The reason for the warn.
- `moderator`: The ID of the moderator who performed the warn.
