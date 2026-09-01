if(CONFIG_SHIELD_TORABO_TSUKI_LP_LEFT OR CONFIG_SHIELD_TORABO_TSUKI_LP_RIGHT)
  zephyr_library()
  zephyr_include_directories(${APPLICATION_SOURCE_DIR}/include)
  zephyr_library_sources(src/board.c src/mini_trackpad_init_reg.c)
  zephyr_library_sources_ifdef(CONFIG_TORABO_SPLIT_PERIPHERAL_ADV_RECOVERY
    src/split_peripheral_adv_recovery.c)
endif()
