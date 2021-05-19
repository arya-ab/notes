# notes

"<p>Platform token grant specifically used for performing token grant using platform, e.g. Steam, Justice, etc. The endpoint automatically create an account if the account associated with the platform is not exists yet.\n\t\t\tThis endpoint requires all requests to have Authorization header set with Basic access authentication\n\t\t\tconstructed from client id and client secret. For publisher-game namespace schema : Specify only either platform_token or device_id. Device token grant\n\t\t\tshould be requested along with device_id parameter against game namespace. Another 3rd party platform token grant should be requested\n\t\t\talong with platform_token parameter against publisher namespace.</p>\n\t\t\t<h2>Supported platforms:</h2>\n\t\t\t<ul>\n\t\t\t\t<li><strong>steam</strong>: The platform_token's value is the authentication code returned by Steam.</li>\n\t\t\t\t<li><strong>steamopenid</strong>: Steam's user authentication method using OpenID 2.0. The platform_token's value is URL generated by Steam on web authentication</li>\n\t\t\t\t<li><strong>facebook</strong>: The platform_token's value is the authorization code returned by Facebook OAuth</li>\n\t\t\t\t<li><strong>google</strong>: The platform_token's value is the authorization code returned by Google OAuth</li>\n\t\t\t\t<li><strong>oculus</strong>: The platform_token's value is a string composed of Oculus's user ID and the nonce separated by a colon (:).</li>\n\t\t\t\t<li><strong>twitch</strong>: The platform_token's value is the authorization code returned by Twitch OAuth.</li>\n\t\t\t\t<li><strong>discord</strong>: The platform_token's value is the authorization code returned by Discord OAuth</li>\n\t\t\t\t<li><strong>android</strong>: The device_id is the Androidâ€™s device ID</li>\n\t\t\t\t<li><strong>ios</strong>: The device_id is the iOS's device ID.</li>\n\t\t\t\t<li><strong>device</strong>: Every device that does'nt run Android and iOS is categorized as a device. The device_id is the device's ID.</li>\n\t\t\t\t<li><strong>justice</strong>: The platform_tokenâ€™s value is the designated user's access token.</li>\n\t\t\t</ul>\n\t\t\t<h2>Access Token Content</h2>\n\t\t\t<p>Following is the access token's content:</p>\n\t\t\t<ul>\n\t\t\t<li>\n\t\t\t\t<p><strong>namespace</strong>. It is the namespace the token was generated from.</p>\n\t\t\t</li>\n\t\t\t<li>\n\t\t\t\t<p><strong>display_name</strong>. The display name of the sub. It is empty if the token is generated from the client credential</p>\n\t\t\t</li>\n\t\t\t<li>\n\t\t\t\t<p><strong>roles</strong>. The sub's roles. It is empty if the token is generated from the client credential</p>\n\t\t\t</li>\n\t\t\t<li>\n\t\t\t\t<p><strong>permissions</strong>. The sub or aud' permissions</p>\n\t\t\t</li>\n\t\t\t<li>\n\t\t\t\t<p><strong>bans</strong>. The sub's list of bans. It is used by the IAM client for validating the token.</p>\n\t\t\t</li>\n\t\t\t<li>\n\t\t\t\t<p><strong>jflgs</strong>. It stands for Justice Flags. It is a special flag used for storing additional status information regarding the sub. It is implemented as a bit mask. Following explains what each bit represents:</p>\n\t\t\t<ul>\n\t\t\t\t<li><p>1: Email Address Verified</p></li>\n\t\t\t\t<li><p>2: Phone Number Verified</p></li>\n\t\t\t\t<li><p>4: Anonymous</p></li>\n\t\t\t</ul>\n\t\t\t</li>\n\t\t\t<li>\n\t\t\t\t<p><strong>aud</strong>. The aud is the client ID.</p>\n\t\t\t</li>\n\t\t\t<li>\n\t\t\t\t<p><strong>iat</strong>. The time the token issues at. It is in Epoch time format</p>\n\t\t\t</li>\n\t\t\t<li>\n\t\t\t\t<p><strong>exp</strong>. The time the token expires. It is in Epoch time format</p>\n\t\t\t</li>\n\t\t\t<li>\n\t\t\t\t<p><strong>sub</strong>. The UserID. The sub is omitted if the token is generated from client credential</p>\n\t\t\t</li>\n\t\t\t<h2>Bans</h2>\n\t\t\t<p>The JWT contains user's active bans with its expiry date. List of ban types can be obtained from /bans.</p><br>action code : 10704",
"operationId": "PlatformTokenGrantV3"
