# Go-live checklist

`get_setup_status` is the source of truth for what is missing. Typical order:

1. The organisation exists (`create_organization`) and the user accepted the data processing agreement.
2. Profile: name, description (at least 80 characters), logo, brand colours (`update_organization_profile`, `apply_brand_colors`).
3. Billing address.
4. Payments connected by the user on the provider's own site (`connect_payments`, then `get_setup_status`).
5. When the status says the organisation can go live: `go_live`, after the user confirms.

Pages can be built as drafts before the organisation is live. Publishing needs it to be live.
