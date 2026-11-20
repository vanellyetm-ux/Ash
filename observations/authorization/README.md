# Independent Authorization Boundary

A future PONS replacement must not be an authorization bypass. Decisions must be issued independently of the code/artifact being changed and bind reviewer identity, cryptographic signature, exact repository/scope, content digest, action, expiry/freshness, revocation state, and explicit human confirmation. Missing, invalid, stale, revoked, or out-of-scope evidence means DENY. A mutable boolean, model response, or file under review cannot authorize itself. This is a proposed policy, not a configured authorization service.
