# Authentication Checklist

## Login
- [ ] Valid credentials → success login
- [ ] Invalid credentials → error message
- [ ] Empty fields → validation error
- [ ] Password masking works
- [ ] Login from multiple devices
- [ ] Session expiration

## Registration
- [ ] Required fields check
- [ ] Email/Phone validation format
- [ ] Password strength enforcement
- [ ] Consent to Privacy Policy mandatory
- [ ] Unique email/phone check

## Recovery
- [ ] "Forgot password" screen visible
- [ ] Correct reset link sent
- [ ] Token expiration
- [ ] Password change success

## Security
- [ ] Rate limiting on login
- [ ] Block after multiple failed attempts
- [ ] 2FA present (if applicable)
