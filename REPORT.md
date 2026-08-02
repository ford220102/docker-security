# Raport skanowania podatności obrazów Docker
## Skanowanie pełne — 58 obrazów (29 unikalnych × 2 skanery)

**Data skanowania:** 2026-08-02  
**Skanery:** Grype v0.115.0 + Trivy v0.71.2  
**Środowisko:** Dockhand (local) + GitHub Security  
**Repozytorium:** ford220102/docker-security

---

## Podsumowanie ogólne

| Metryka | Wartość |
|---------|---------|
| Skanowane obrazy | 58 (29 unikalnych × 2 skanery) |
| Łączne znalezienia | 9 481 CVE |
| Critical | 289 |
| High | 2 559 |
| Medium | 4 339 |
| Low | 2 294 |

---

## Wyniki per obraz (Grype + Trivy)

### 🔴 Krytyczne problemy (Critical > 0)

| Obraz | Grype C/H/M/L | Trivy C/H/M/L |
|-------|---------------|---------------|
| ghcr.io/flaresolverr/flaresolverr:latest | 603 / 2058 / 2425 / 159 | 166 / 1851 / 2029 / 1300 |
| ghcr.io/immich-app/immich-server:release | 47 / 116 / 135 / 20 | 29 / 88 / 174 / 201 |
| ghcr.io/immich-app/postgres:14-vectorchord0.4.3-pgvectors0.2.0 | 39 / 187 / 181 / 29 | 27 / 123 / 222 / 194 |
| ghcr.io/immich-app/immich-machine-learning:release | 15 / 90 / 122 / 17 | 11 / 51 / 101 / 143 |
| lscr.io/linuxserver/bazarr:latest | 17 / 114 / 52 / 4 | 0 / 2 / 0 / 0 |
| valkey/valkey:9 | 7 / 19 / 45 / 4 | 4 / 18 / 54 / 65 |
| valkey/valkey@sha256:8e8d... | 7 / 19 / 45 / 4 | 4 / 18 / 54 / 65 |
| portainer/portainer-ce:latest | 2 / 11 / 7 / 0 | 0 / 10 / 5 / 0 |
| postgres:15-alpine | 1 / 18 / 21 / 2 | 1 / 14 / 21 / 2 |
| lancachenet/lancache-dns:latest | 2 / 19 / 267 / 27 | 1 / 14 / 43 / 13 |
| ghcr.io/homarr-labs/homarr:latest | 2 / 16 / 19 / 4 | 2 / 16 / 16 / 3 |
| anchore/grype:v0.115.0 | 0 / 8 / 5 / 0 | 0 / 8 / 4 / 0 |
| aquasec/trivy:0.71.2 | 8 / 17 / 26 / 3 | 0 / 17 / 29 / 3 |
| cyfershepard/jellystat:latest | 8 / 47 / 72 / 9 | 6 / 46 / 80 / 76 |
| ghcr.io/wg-easy/wg-easy:14 | 10 / 74 / 64 / 18 | 5 / 49 / 48 / 45 |
| eclipse-temurin:21-jdk | 0 / 4 / 251 / 91 | 0 / 5 / 88 / 14 |
| eclipse-temurin:21-jre | 0 / 4 / 187 / 19 | 0 / 5 / 88 / 6 |
| lscr.io/linuxserver/lidarr:latest | 0 / 36 / 26 / 1 | 0 / 0 / 12 / 0 |
| lscr.io/linuxserver/jellyfin:latest | 0 / 5 / 207 / 31 | 0 / 5 / 97 / 12 |

### 🟡 Bez krytycznych (Critical = 0)

| Obraz | Grype C/H/M/L | Trivy C/H/M/L |
|-------|---------------|---------------|
| media-stack-desktop-3d:latest | 0 / 4 / 187 / 19 | 0 / 5 / 88 / 6 |
| lancachenet/monolithic:latest | 0 / 0 / 218 / 28 | 0 / 0 / 27 / 14 |
| fnsys/dockhand:latest | 0 / 6 / 4 / 0 | 0 / 0 / 0 / 0 |
| adminer:latest | 0 / 0 / 5 / 0 | 0 / 0 / 0 / 0 |
| lscr.io/linuxserver/prowlarr:latest | 0 / 0 / 8 / 0 | 0 / 0 / 0 / 0 |
| lscr.io/linuxserver/radarr:latest | 0 / 12 / 14 / 0 | 0 / 0 / 0 / 0 |
| lscr.io/linuxserver/qbittorrent:latest | 0 / 5 / 16 / 0 | 0 / 0 / 0 / 0 |
| lscr.io/linuxserver/sonarr:latest | 0 / 1 / 20 / 0 | 0 / 1 / 12 / 0 |
| python:3.12-alpine | 0 / 10 / 21 / 3 | 0 / 0 / 4 / 1 |

---

## Top 5 obrazów wymagających naprawy (najwięcej CVE)

1. **ghcr.io/flaresolverr/flaresolverr:latest** — 603 Critical (Grype) / 166 Critical (Trivy) → **PRIORYTET 1**
2. **ghcr.io/immich-app/immich-server:release** — 47 Critical (Grype) / 29 Critical (Trivy) → **PRIORYTET 2**
3. **ghcr.io/immich-app/postgres:14-vectorchord0.4.3-pgvectors0.2.0** — 39 Critical (Grype) / 27 Critical (Trivy) → **PRIORYTET 3**
4. **ghcr.io/immich-app/immich-machine-learning:release** — 15 Critical (Grype) / 11 Critical (Trivy) → **PRIORYTET 4**
5. **lscr.io/linuxserver/bazarr:latest** — 17 Critical (Grype) → **PRIORYTET 5**

---

## Status napraw

| Status | Opis |
|--------|------|
| ✅ Skanowane | Wszystkie 58 skanów (29 obrazów × 2 skanery) zakończonych |
| ✅ SARIF upload | Wyniki przesłane do GitHub Security (ford220102/docker-security) |
| ✅ Dockhand DB | 116 rekordów w vulnerability_scans |
| ✅ Workflow | GitHub Actions workflow aktywny (push + schedule + manual) |
| ⏳ Naprawa CVE | W trakcie — wymagane aktualizacje obrazów |

---

## Rekomendacje

1. **flaresolverr** — najbardziej krytyczny obraz, wymaga natychmiastowej aktualizacji lub zamiany na alternatywę
2. **immich** — 47+29=76 krytycznych CVE, wymaga aktualizacji do najnowszej wersji
3. **immich-postgres** — 39+27=66 krytycznych CVE, wymaga aktualizacji
4. **bazarr** — 17 krytycznych CVE (Grype), wymaga aktualizacji
5. **valkey** — 7+4=11 krytycznych CVE, wymaga aktualizacji
6. **wg-easy** — 10+5=15 krytycznych CVE, wymaga aktualizacji
7. **jellyfin** — 207+97=304 medium CVE, wymaga aktualizacji

---

*Raport wygenerowany automatycznie przez Dockhand + GitHub Actions*
