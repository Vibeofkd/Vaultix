# Dispute Deadline Implementation TODO

## Steps:
- [x] 1. Update Escrow entity (`escrow.entity.ts`): add `disputeDeadline` column, `Dispute` import, and `OneToOne` decorator imports
- [x] 2. Update EscrowEvent enum (`escrow-event.entity.ts`): add `DISPUTE_TIMEOUT = 'dispute_timeout'`
- [x] 3. Fix Escrow controller (`escrow.controller.ts`): add missing `AdminGuard` import
- [x] 4. Fix Escrow service (`escrow.service.ts`): replace string cast with `EscrowEventType.DISPUTE_TIMEOUT`
- [ ] 5. Update on-chain types (`lib.rs`): add `dispute_deadline: u64` to `Escrow` and `EscrowEntryV2` structs; update mapping functions
- [ ] 6. Update on-chain `raise_dispute` (`lib.rs`): set `dispute_deadline` when raising a dispute
- [ ] 7. Implement on-chain `trigger_default_resolution` (`lib.rs`): auto-resolve with 50/50 split after deadline
- [ ] 8. Add on-chain tests (`test.rs`): verify deadline setting and default resolution behavior
- [ ] 9. Verify backend builds (`npm run build`)
- [ ] 10. Verify on-chain tests pass (`cargo test`)

**Next:** Start editing files

