# Git συνεργασία ομάδας

Αυτό το project ακολουθεί υποχρεωτικά ροή με Pull Requests και έγκριση πριν το merge.

## Κανόνες branch

- Μην κάνεις commit απευθείας στο `main`.
- Δημιούργησε branch ανά εργασία:
  - `feature/<short-description>`
  - `fix/<short-description>`
  - `docs/<short-description>`
  - `chore/<short-description>`

Παράδειγμα:

```bash
git checkout main
git pull origin main
git checkout -b feature/bid-validation
```

## Κανόνες commit message

Χρησιμοποίησε σύντομα, καθαρά μηνύματα:

- `feat: add bid validation for negative values`
- `fix: prevent duplicate login session`
- `docs: update demo run instructions`

## Ροή Pull Request

1. Κάνε push το branch σου:
   - `git push -u origin <branch-name>`
2. Άνοιξε PR προς `main`.
3. Συμπλήρωσε υποχρεωτικά το PR template (Τι/Γιατί/Testing).
4. Βάλε reviewer τον υπεύθυνο έγκρισης.
5. Κάνε resolve όλα τα σχόλια review.
6. Κάνε merge μόνο όταν υπάρχει έγκριση και πράσινο CI.

## Καθημερινός ρυθμός ομάδας

- Πριν ξεκινήσεις δουλειά:
  - `git checkout main`
  - `git pull origin main`
- Στο τέλος της ημέρας:
  - κάνε push το branch σου
  - ενημέρωσε το PR με τι ολοκληρώθηκε και τι μένει
- Για τον approver:
  - καθημερινός κύκλος review σε ανοιχτά PRs
  - `Request changes` με συγκεκριμένα σχόλια ή `Approve` αν είναι έτοιμο

## Merge strategy

Προτιμάμε `Squash and merge` για καθαρό ιστορικό στο `main`.
