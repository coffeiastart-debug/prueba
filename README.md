 docker compose exec -u root backend rm -rf /app/.cache/camoufox/addons/UBO

  docker compose exec backend python -c "from camoufox.addons import DefaultAddons, maybe_download_addons;
  maybe_download_addons([DefaultAddons.UBO])"
docker compose exec -u root backend rm -rf /app/.cache/camoufox/addons/UBO

ocker compose exec backend python -c "from camoufox.addons import DefaultAddons, maybe_download_addons; maybe_download_addons([DefaultAddons.UBO])"
